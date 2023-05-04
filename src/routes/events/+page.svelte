<script>
	import { fairDates } from '$lib/Schedule/fairDates';
	import { day01events } from '$lib/Schedule/day01Events';
	import { Tab, TabGroup } from '@skeletonlabs/skeleton';

	let tabSet = 0;
</script>

<section class="hero bg-section flex flex-col">
	<img src="/img/event-banner.webp" alt="Events" class="hidden lg:inline-block p-4" />
	<img src="/img/event-banner02.webp" alt="Events" class="lg:hidden p-4" />

	<TabGroup
		justify="justify-center"
		active="variant-filled-primary"
		hover="hover:variant-soft-primary"
		rounded="rounded-lg"
		border=""
		flex="flex-1"
	>
    <!-- TODO: Fix TabGroup spacing on mobile -->
		{#each fairDates as date}
			<Tab bind:group={tabSet} name="tab{date.num}" value={date.tab}>
				<span class="text-2xl">{date.day}</span><br />
				<span class="text-2xl">Jul</span><br />
				<span class="text-5xl">{date.num}</span>
			</Tab>
		{/each}
		<svelte:fragment slot="panel">
			{#if tabSet === 0}
				<div
					class="grid grid-cols-2 md:grid-cols-4 gap-4 p-8 my-8 w-11/12 mx-auto bg-surface-700 rounded-lg outline outline-white"
				>
					{#each day01events as event}
						<div class="text-3xl">{event.time}</div>
						<div class="col-span-2">
							{#if event.category === "culture"}
                <a href="/culture" class="decoration-transparent">
                  <span class="chip variant-filled-secondary">Culture</span><br>
                </a>
              {:else if event.category === "family"}
                <a href="/family" class="decoration-transparent">
                  <span class="chip variant-filled-tertiary">Family Fun</span><br>
                </a>
              {:else if event.category === "stickball"}
                <a href="/stickball" class="decoration-transparent">
                  <span class="chip variant-filled-success">Stickball</span><br>
                </a>
              {:else if event.category === "pageant"}
                <a href="/pageant" class="decoration-transparent">
                  <span class="chip variant-filled-warning">Pageant</span><br>
                </a>
              {:else if event.category === "competitions"}
                <a href="/competitions" class="decoration-transparent">
                  <span class="chip variant-filled-error">Competitions</span><br>
                </a>
              {/if}
							{event.title}
						</div>
						<div class="col-span-2 md:col-span-1">{event.location}</div>
						<hr class="col-span-2 md:col-span-4" />
					{/each}
					<div class="col-span-2 md:col-span-4 italic text-center">End of day</div>
				</div>
			{:else if tabSet === 1}
      <div
      class="grid grid-cols-2 md:grid-cols-4 gap-4 p-8 mb-20 w-11/12 mx-auto bg-surface-700 rounded-lg outline outline-white"
    >
      {#each day01events as event}
        <div class="text-3xl">{event.time}</div>
        <div class="col-span-2">
          {#if event.category === "culture"}
            <a href="/culture" class="decoration-transparent">
              <span class="chip variant-filled-secondary">Culture</span><br>
            </a>
          {:else if event.category === "family"}
            <a href="/family" class="decoration-transparent">
              <span class="chip variant-filled-tertiary">Family Fun</span><br>
            </a>
          {:else if event.category === "stickball"}
            <a href="/stickball" class="decoration-transparent">
              <span class="chip variant-filled-success">Stickball</span><br>
            </a>
          {:else if event.category === "pageant"}
            <a href="/pageant" class="decoration-transparent">
              <span class="chip variant-filled-warning">Pageant</span><br>
            </a>
          {:else if event.category === "competitions"}
            <a href="/competitions" class="decoration-transparent">
              <span class="chip variant-filled-error">Competitions</span><br>
            </a>
          {/if}
          {event.title}
        </div>
        <div class="col-span-2 md:col-span-1">{event.location}</div>
        <hr class="col-span-2 md:col-span-4" />
      {/each}
      <div class="col-span-2 md:col-span-4 italic text-center">End of day</div>
    </div>
			{:else if tabSet === 2}
      <div
      class="grid grid-cols-2 md:grid-cols-4 gap-4 p-8 mb-20 w-11/12 mx-auto bg-surface-700 rounded-lg outline outline-white"
    >
      {#each day01events as event}
        <div class="text-3xl">{event.time}</div>
        <div class="col-span-2">
          {#if event.category === "culture"}
            <a href="/culture" class="decoration-transparent">
              <span class="chip variant-filled-secondary">Culture</span><br>
            </a>
          {:else if event.category === "family"}
            <a href="/family" class="decoration-transparent">
              <span class="chip variant-filled-tertiary">Family Fun</span><br>
            </a>
          {:else if event.category === "stickball"}
            <a href="/stickball" class="decoration-transparent">
              <span class="chip variant-filled-success">Stickball</span><br>
            </a>
          {:else if event.category === "pageant"}
            <a href="/pageant" class="decoration-transparent">
              <span class="chip variant-filled-warning">Pageant</span><br>
            </a>
          {:else if event.category === "competitions"}
            <a href="/competitions" class="decoration-transparent">
              <span class="chip variant-filled-error">Competitions</span><br>
            </a>
          {/if}
          {event.title}
        </div>
        <div class="col-span-2 md:col-span-1">{event.location}</div>
        <hr class="col-span-2 md:col-span-4" />
      {/each}
      <div class="col-span-2 md:col-span-4 italic text-center">End of day</div>
    </div>
			{:else if tabSet === 3}
      <div
      class="grid grid-cols-2 md:grid-cols-4 gap-4 p-8 mb-20 w-11/12 mx-auto bg-surface-700 rounded-lg outline outline-white"
    >
      {#each day01events as event}
        <div class="text-3xl">{event.time}</div>
        <div class="col-span-2">
          {#if event.category === "culture"}
            <a href="/culture" class="decoration-transparent">
              <span class="chip variant-filled-secondary">Culture</span><br>
            </a>
          {:else if event.category === "family"}
            <a href="/family" class="decoration-transparent">
              <span class="chip variant-filled-tertiary">Family Fun</span><br>
            </a>
          {:else if event.category === "stickball"}
            <a href="/stickball" class="decoration-transparent">
              <span class="chip variant-filled-success">Stickball</span><br>
            </a>
          {:else if event.category === "pageant"}
            <a href="/pageant" class="decoration-transparent">
              <span class="chip variant-filled-warning">Pageant</span><br>
            </a>
          {:else if event.category === "competitions"}
            <a href="/competitions" class="decoration-transparent">
              <span class="chip variant-filled-error">Competitions</span><br>
            </a>
          {/if}
          {event.title}
        </div>
        <div class="col-span-2 md:col-span-1">{event.location}</div>
        <hr class="col-span-2 md:col-span-4" />
      {/each}
      <div class="col-span-2 md:col-span-4 italic text-center">End of day</div>
    </div>
			{:else if tabSet === 4}
      <div
      class="grid grid-cols-2 md:grid-cols-4 gap-4 p-8 mb-20 w-11/12 mx-auto bg-surface-700 rounded-lg outline outline-white"
    >
      {#each day01events as event}
        <div class="text-3xl">{event.time}</div>
        <div class="col-span-2">
          {#if event.category === "culture"}
            <a href="/culture" class="decoration-transparent">
              <span class="chip variant-filled-secondary">Culture</span><br>
            </a>
          {:else if event.category === "family"}
            <a href="/family" class="decoration-transparent">
              <span class="chip variant-filled-tertiary">Family Fun</span><br>
            </a>
          {:else if event.category === "stickball"}
            <a href="/stickball" class="decoration-transparent">
              <span class="chip variant-filled-success">Stickball</span><br>
            </a>
          {:else if event.category === "pageant"}
            <a href="/pageant" class="decoration-transparent">
              <span class="chip variant-filled-warning">Pageant</span><br>
            </a>
          {:else if event.category === "competitions"}
            <a href="/competitions" class="decoration-transparent">
              <span class="chip variant-filled-error">Competitions</span><br>
            </a>
          {/if}
          {event.title}
        </div>
        <div class="col-span-2 md:col-span-1">{event.location}</div>
        <hr class="col-span-2 md:col-span-4" />
      {/each}
      <div class="col-span-2 md:col-span-4 italic text-center">End of day</div>
    </div>
			{:else if tabSet === 5}
      <div
      class="grid grid-cols-2 md:grid-cols-4 gap-4 p-8 mb-20 w-11/12 mx-auto bg-surface-700 rounded-lg outline outline-white"
    >
      {#each day01events as event}
        <div class="text-3xl">{event.time}</div>
        <div class="col-span-2">
          {#if event.category === "culture"}
            <a href="/culture" class="decoration-transparent">
              <span class="chip variant-filled-secondary">Culture</span><br>
            </a>
          {:else if event.category === "family"}
            <a href="/family" class="decoration-transparent">
              <span class="chip variant-filled-tertiary">Family Fun</span><br>
            </a>
          {:else if event.category === "stickball"}
            <a href="/stickball" class="decoration-transparent">
              <span class="chip variant-filled-success">Stickball</span><br>
            </a>
          {:else if event.category === "pageant"}
            <a href="/pageant" class="decoration-transparent">
              <span class="chip variant-filled-warning">Pageant</span><br>
            </a>
          {:else if event.category === "competitions"}
            <a href="/competitions" class="decoration-transparent">
              <span class="chip variant-filled-error">Competitions</span><br>
            </a>
          {/if}
          {event.title}
        </div>
        <div class="col-span-2 md:col-span-1">{event.location}</div>
        <hr class="col-span-2 md:col-span-4" />
      {/each}
      <div class="col-span-2 md:col-span-4 italic text-center">End of day</div>
    </div>
			{:else if tabSet === 6}
      <div
      class="grid grid-cols-2 md:grid-cols-4 gap-4 p-8 mb-20 w-11/12 mx-auto bg-surface-700 rounded-lg outline outline-white"
    >
      {#each day01events as event}
        <div class="text-3xl">{event.time}</div>
        <div class="col-span-2">
          {#if event.category === "culture"}
            <a href="/culture" class="decoration-transparent">
              <span class="chip variant-filled-secondary">Culture</span><br>
            </a>
          {:else if event.category === "family"}
            <a href="/family" class="decoration-transparent">
              <span class="chip variant-filled-tertiary">Family Fun</span><br>
            </a>
          {:else if event.category === "stickball"}
            <a href="/stickball" class="decoration-transparent">
              <span class="chip variant-filled-success">Stickball</span><br>
            </a>
          {:else if event.category === "pageant"}
            <a href="/pageant" class="decoration-transparent">
              <span class="chip variant-filled-warning">Pageant</span><br>
            </a>
          {:else if event.category === "competitions"}
            <a href="/competitions" class="decoration-transparent">
              <span class="chip variant-filled-error">Competitions</span><br>
            </a>
          {/if}
          {event.title}
        </div>
        <div class="col-span-2 md:col-span-1">{event.location}</div>
        <hr class="col-span-2 md:col-span-4" />
      {/each}
      <div class="col-span-2 md:col-span-4 italic text-center">End of day</div>
    </div>
			{:else if tabSet === 7}
      <div
      class="grid grid-cols-2 md:grid-cols-4 gap-4 p-8 mb-20 w-11/12 mx-auto bg-surface-700 rounded-lg outline outline-white"
    >
      {#each day01events as event}
        <div class="text-3xl">{event.time}</div>
        <div class="col-span-2">
          {#if event.category === "culture"}
            <a href="/culture" class="decoration-transparent">
              <span class="chip variant-filled-secondary">Culture</span><br>
            </a>
          {:else if event.category === "family"}
            <a href="/family" class="decoration-transparent">
              <span class="chip variant-filled-tertiary">Family Fun</span><br>
            </a>
          {:else if event.category === "stickball"}
            <a href="/stickball" class="decoration-transparent">
              <span class="chip variant-filled-success">Stickball</span><br>
            </a>
          {:else if event.category === "pageant"}
            <a href="/pageant" class="decoration-transparent">
              <span class="chip variant-filled-warning">Pageant</span><br>
            </a>
          {:else if event.category === "competitions"}
            <a href="/competitions" class="decoration-transparent">
              <span class="chip variant-filled-error">Competitions</span><br>
            </a>
          {/if}
          {event.title}
        </div>
        <div class="col-span-2 md:col-span-1">{event.location}</div>
        <hr class="col-span-2 md:col-span-4" />
      {/each}
      <div class="col-span-2 md:col-span-4 italic text-center">End of day</div>
    </div>
			{:else if tabSet === 8}
      <div
      class="grid grid-cols-2 md:grid-cols-4 gap-4 p-8 mb-20 w-11/12 mx-auto bg-surface-700 rounded-lg outline outline-white"
    >
      {#each day01events as event}
        <div class="text-3xl">{event.time}</div>
        <div class="col-span-2">
          {#if event.category === "culture"}
            <a href="/culture" class="decoration-transparent">
              <span class="chip variant-filled-secondary">Culture</span><br>
            </a>
          {:else if event.category === "family"}
            <a href="/family" class="decoration-transparent">
              <span class="chip variant-filled-tertiary">Family Fun</span><br>
            </a>
          {:else if event.category === "stickball"}
            <a href="/stickball" class="decoration-transparent">
              <span class="chip variant-filled-success">Stickball</span><br>
            </a>
          {:else if event.category === "pageant"}
            <a href="/pageant" class="decoration-transparent">
              <span class="chip variant-filled-warning">Pageant</span><br>
            </a>
          {:else if event.category === "competitions"}
            <a href="/competitions" class="decoration-transparent">
              <span class="chip variant-filled-error">Competitions</span><br>
            </a>
          {/if}
          {event.title}
        </div>
        <div class="col-span-2 md:col-span-1">{event.location}</div>
        <hr class="col-span-2 md:col-span-4" />
      {/each}
      <div class="col-span-2 md:col-span-4 italic text-center">End of day</div>
    </div>
			{:else if tabSet === 9}
      <div
      class="grid grid-cols-2 md:grid-cols-4 gap-4 p-8 mb-20 w-11/12 mx-auto bg-surface-700 rounded-lg outline outline-white"
    >
      {#each day01events as event}
        <div class="text-3xl">{event.time}</div>
        <div class="col-span-2">
          {#if event.category === "culture"}
            <a href="/culture" class="decoration-transparent">
              <span class="chip variant-filled-secondary">Culture</span><br>
            </a>
          {:else if event.category === "family"}
            <a href="/family" class="decoration-transparent">
              <span class="chip variant-filled-tertiary">Family Fun</span><br>
            </a>
          {:else if event.category === "stickball"}
            <a href="/stickball" class="decoration-transparent">
              <span class="chip variant-filled-success">Stickball</span><br>
            </a>
          {:else if event.category === "pageant"}
            <a href="/pageant" class="decoration-transparent">
              <span class="chip variant-filled-warning">Pageant</span><br>
            </a>
          {:else if event.category === "competitions"}
            <a href="/competitions" class="decoration-transparent">
              <span class="chip variant-filled-error">Competitions</span><br>
            </a>
          {/if}
          {event.title}
        </div>
        <div class="col-span-2 md:col-span-1">{event.location}</div>
        <hr class="col-span-2 md:col-span-4" />
      {/each}
      <div class="col-span-2 md:col-span-4 italic text-center">End of day</div>
    </div>
			{/if}
		</svelte:fragment>
	</TabGroup>
</section>

<style>
	.bg-section {
		background: center / cover url('/isometric.svg'), linear-gradient(to bottom right, red, maroon);
		background-blend-mode: darken;
	}
</style>
