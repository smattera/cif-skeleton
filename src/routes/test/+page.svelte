<script>
	import { readable } from 'svelte/store';
  import { Render, Subscribe, createTable } from 'svelte-headless-table';
  import { addSortBy, addColumnFilters } from 'svelte-headless-table/plugins';

  const data = readable([
    { time: "6:00 PM", category: "Stickball", title: "Opening Ceremonies, Fallen Tushka Ceremony, & Happy Feet Social Dancers" },
    { time: "7:00 PM", category: "Stickball", title: "Alla Tik Tóli (14-17) Exhibition Game" },
    { time: "8:00 PM", category: "Stickball", title: "Legends: Men's (50+) Exhibition Game: North VS South" },
    { time: "9:00 PM", category: "Stickball", title: "Women's (35+) Exhibition Game: North VS South" },
    { time: "10:00 PM", category: "Stickball", title: "Men's Division: Game 1" },
  ]);

  const table = createTable(data, {
    sort: addSortBy(),
    filter: addColumnFilters(),
  });

  const columns = table.createColumns([
    table.column({
      header: 'Time',
      accessor: 'time',
    }),
    table.column({
      header: 'Category',
      accessor: 'category',
    }),
    table.column({
      header: 'Title',
      accessor: 'title',
    })
  ]);

  const {
    headerRows,
    rows,
    tableAttrs,
    tableBodyAttrs,
  } = table.createViewModel(columns);


</script>

<table {...$tableAttrs}>
  <thead>
    {#each $headerRows as headerRow (headerRow.id)}
    <Subscribe rowAttrs={headerRow.attrs()} let:rowAttrs>
      <tr {...rowAttrs}>
        {#each headerRow.cells as cell (cell.id)}
          <Subscribe attrs={cell.attrs()} let:attrs>
            <th {...attrs}>
              <Render of={cell.render()} />
            </th>
          </Subscribe>
        {/each}
      </tr>
    </Subscribe>
    {/each}
  </thead>
  <tbody {...$tableBodyAttrs}>
    {#each $rows as row (row.id)}
      <Subscribe rowAttrs={row.attrs()} let:rowAttrs>
        <tr {...rowAttrs}>
          {#each row.cells as cell (cell.id)}
            <Subscribe attrs={cell.attrs()} let:attrs>
              <td {...attrs}>
                <Render of={cell.render()} />
              </td>
            </Subscribe>
          {/each}
        </tr>
      </Subscribe>
    {/each}
  </tbody>
</table>
