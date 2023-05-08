<script>
	import { page } from "$app/stores";
	import { drawerStore } from '@skeletonlabs/skeleton';

	function drawerClose() {
		drawerStore.close();
	}

	const pages = [
    { name: "Home", href: "/", icon: "home", viewBox: "0 0 24 24" },
    { name: "Events", href: "/events", icon: "events", viewBox: "0 96 960 960" },
    { name: "Culture", href: "/culture", icon: "culture", viewBox: "0 0 48 48" },
		{ name: "Tushka Village", href: "/culture#tushka" },
		{ name: "Danceground", href: "/culture#danceground" },
		{ name: "Arts & Crafts", href: "/culture#arts" },
		{ name: "Traditional Food", href: "#culture#food" },
    { name: "Family Fun", href: "/family", icon: "family", viewBox: "0 96 960 960" },
		{ name: "Áyi̱pa Village", href: "family#ayipa" },
		{ name: "Shawi's Zone", href: "family#shawi" },
		{ name: "O̱ssi Cove", href: "family#ossi" },
    { name: "Stickball", href: "/stickball", icon: "stickball", viewBox: "0 0 48 48" },
		{ name: "Men's Division", href: "/stickball#mens" },
		{ name: "Women's Division", href: "/stickball#womens" },
		{ name: "Men's (35+) Division", href: "/stickball#mens35" },
		{ name: "Tulli Okchi Ishko", href: "/stickball#tulli" },
		{ name: "Pushmataha Division", href: "/stickball#push" },
    { name: "Pageant", href: "/pageant", icon: "home", viewBox: "0 0 24 24" },
    { name: "Competitions", href: "/competitions", icon: "competitions", viewBox: "0 0 48 48" },
		{ name: "Rez Run", href: "/competitions#rezrun" },
		{ name: "Iron Warrior", href: "/competitions#ironwarrior" },
		{ name: "Cornhole", href: "/competitions#cornhole" },
		{ name: "Volleyball", href: "/competitions#volleyball" },
		{ name: "Gospel Night", href: "/competitions#gospelnight" },
		{ name: "Little CIF Pageant", href: "/competitions#pageant" },
		{ name: "Frybread Making", href: "/competitions#frybread" },
		{ name: "Watermelon Eating", href: "/competitions#watermelon" },
    { name: "Fair Map", href: "/map", icon: "map", viewBox: "0 96 960 960" },
  ];
	$: currentRoute = $page.url.pathname;
</script>

<nav class="list-nav p-2">
	<ul>
		{#each pages as page}
		<li>
			<a on:click={drawerClose} href={page.href} class:bg-success-active-token={currentRoute == page.href}>
				{#if page.icon}
				<svg viewBox={page.viewBox} fill="currentColor">
					<use xlink:href="#icon-{page.icon}"></use>
				</svg>
				{:else}
				<div class="w-10"></div>
				{/if}
				{page.name}
			</a>
		</li>
		{/each}
	</ul>
</nav>

<style>
	svg {
  height: 30px;
  width: auto;
  fill: currentColor;
  vertical-align: bottom;
	margin-right: 10px;
	}
</style>
