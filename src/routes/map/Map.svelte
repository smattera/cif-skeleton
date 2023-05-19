<script>
	import { onDestroy, setContext } from 'svelte';
	import { mapbox, key } from './mapbox.js';

	setContext(key, {
		getMap: () => map,
	});

	// @ts-ignore
	export let lat;
	// @ts-ignore
	export let lon;
	// @ts-ignore
	export let zoom;

	// @ts-ignore
	let container;
	/**
	 * @type {{ remove: () => void; }}
	 */
	let map;

	function load() {
		map = new mapbox.Map({
			// @ts-ignore
			container,
			style: 'mapbox://styles/mapbox/streets-v9',
			// @ts-ignore
			center: [lon, lat],
			// @ts-ignore
			zoom,
		});
	}

	onDestroy(() => {
		if (map) map.remove();
	});
</script>

<svelte:head>
	<link
		rel="stylesheet"
		href="https://unpkg.com/mapbox-gl/dist/mapbox-gl.css"
		on:load={load}
	/>
</svelte:head>

<div bind:this={container}>
	{#if map}
		<slot />
	{/if}
</div>

<style>
	div {
		width: 100%;
		height: 100%;
	}
</style>
