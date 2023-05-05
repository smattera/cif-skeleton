<script>
	import { Tab, TabGroup } from "@skeletonlabs/skeleton";
	let tabSet = 0;
</script>

<section class="hero bg-section flex flex-col">
	<img src="/img/event-banner.webp" alt="Events" class="hidden lg:inline-block p-4" />
	<img src="/img/event-banner02.webp" alt="Events" class="lg:hidden p-4" />

	<TabGroup 
		justify="justify-center"
		active="variant-filled-secondary"
		hover="hover:variant-soft-secondary"
		flex="flex-1 lg:flex-none"
		rounded="rounded-xl"
		border=""
		class="w-full"
	>
		<Tab bind:group={tabSet} name="Tushka Village" value={0}>
			<svelte:fragment slot="lead">
				<svg viewBox="0 0 24 24" fill="currentColor">
					<use xlink:href="#icon-home"></use>
				</svg>
			</svelte:fragment>
			Tushka Village
		</Tab>
		<Tab bind:group={tabSet} name="Danceground" value={1}>
			<svelte:fragment slot="lead">
				<svg viewBox="0 0 24 24" fill="currentColor">
					<use xlink:href="#icon-home"></use>
				</svg>
			</svelte:fragment>
			Danceground
		</Tab>
		<Tab bind:group={tabSet} name="Arts & Crafts" value={2}>
			<svelte:fragment slot="lead">
				<svg viewBox="0 0 24 24" fill="currentColor">
					<use xlink:href="#icon-home"></use>
				</svg>
			</svelte:fragment>
			Arts & Crafts
		</Tab>
		<svelte:fragment slot="panel">
			{#if tabSet === 0}
				(tab panel 1 contents)
			{:else if tabSet === 1}
				(tab panel 2 contents)
			{:else if tabSet === 2}
				(tab panel 3 contents)
			{/if}
		</svelte:fragment>
	</TabGroup>

</section>

<style>
	.bg-section {
		background: center / cover url('/isometric.svg'), linear-gradient(to bottom right, blue, midnightblue);
		background-blend-mode: darken;
	}
</style>
