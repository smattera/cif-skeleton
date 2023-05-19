<script lang="ts">
  import { mensTable } from '$lib/Scores/mensGames.js';
  import { Table } from '@skeletonlabs/skeleton';
</script>

<section class="hero bg-section flex flex-col">

  <!-- <img src="/img/event-banner.webp" alt="Events" class="hidden lg:inline-block p-4" />
	<img src="/img/event-banner02.webp" alt="Events" class="lg:hidden p-4" /> -->
	<br><br><br>
  <h1 class="font-bold text-center pb-20">2023 Stickball Coming Soon!</h1>

  <!-- <h2 id="mens">2022 Men's Division<a href="#mens" class="permalink">🔗</a></h2>
  <Table source={mensTable} interactive={true} class="p-4" />

  <h2 id="womens">2022 Women's Division<a href="#womens" class="permalink">🔗</a></h2>
  <Table source={mensTable} interactive={true} class="p-4" />

  <h2 id="mens35">2022 Men's (35+) Division<a href="#mens35" class="permalink">🔗</a></h2>
  <Table source={mensTable} interactive={true} class="p-4" />

  <h2 id="tulli">2022 Tulli Okchi Ishko Division<a href="#tulli" class="permalink">🔗</a></h2>
  <Table source={mensTable} interactive={true} class="p-4" />

  <h2 id="push">2022 Pushmataha Division<a href="#push" class="permalink">🔗</a></h2>
  <Table source={mensTable} interactive={true} class="p-4" /> -->

</section>

<style>
  h2 {
    text-align: center;
    text-transform: uppercase;
    font-weight: bold;
  }
  .bg-section {
		background: center / cover url('/isometric.svg'), linear-gradient(to bottom right, grey, black);
		background-blend-mode: darken;
	}
</style>
