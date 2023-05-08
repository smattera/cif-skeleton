<script lang="ts">
  import "../app.postcss";
  // The ordering of these imports is critical to your app working properly
  import "../theme.postcss";
  // If you have source.organizeImports set to true in VSCode, then it will auto change this ordering
  import "@skeletonlabs/skeleton/styles/all.css";
  // Most of your app wide CSS should be put in this file
  import "../app.postcss";
  import { AppShell, AppBar } from "@skeletonlabs/skeleton";
  import Navigation from "$lib/Navigation/Navigation.svelte";
  import { Drawer, drawerStore } from "@skeletonlabs/skeleton";
  import Icons from "$lib/Icons/Icons.svelte";
	import Footer from "../components/Footer.svelte";

  function drawerOpen(): void {
    drawerStore.open({});
  }
</script>

<Icons />
<Drawer>
  <h2 class="p-4 uppercase font-bold">
    <img
      src="/logos/icon.webp"
      class="h-10 w-auto inline-block pr-0 md:pr-3"
      style="vertical-align:middle"
      alt="Choctaw Indian Fair"
    />Choctaw Indian Fair
  </h2>
  <hr />
  <Navigation />
</Drawer>
<!-- App Shell -->
<AppShell slotSidebarLeft="bg-surface-200/5 w-0 lg:w-64">
  <svelte:fragment slot="sidebarLeft">
    <Navigation />
  </svelte:fragment>
  <svelte:fragment slot="header">
    <!-- App Bar -->
    <AppBar
      gridcolumns="grid-cols-3"
      slotdefault="place-self-center"
      slottrail="place-content-end"
    >
      <svelte:fragment slot="lead">
        <div class="flex items-start">
          <button class="lg:hidden btn btn-sm mr-4" on:click={drawerOpen}>
            <span>
              <svg viewBox="0 0 100 80" class="fill-token w-4 h-4">
                <rect width="100" height="20" />
                <rect y="30" width="100" height="20" />
                <rect y="60" width="100" height="20" />
              </svg>
            </span>
          </button>
        </div>
      </svelte:fragment>
      <strong class="text-xl uppercase">
        <img
          src="/logos/icon.webp"
          class="h-10 w-auto inline-block pr-3"
          style="vertical-align:middle"
          alt="Choctaw Indian Fair"
        />
        <span class="hidden lg:inline-block" style="text-shadow: 0px 0px 10px #aaa">Choctaw Indian Fair</span>
      </strong>
      <svelte:fragment slot="trail">
        <a class="btn variant-filled-success" href="/">
          <svg viewBox="0 96 960 960" fill="currentColor" class="buy-tickets">
            <use xlink:href="#icon-ticket" />
          </svg>
          <span class="hidden lg:inline-block">Buy Tickets</span>
        </a>
      </svelte:fragment>
    </AppBar>
  </svelte:fragment>
  <svelte:fragment slot="pageFooter">
    <Footer />
  </svelte:fragment>
  <!-- Page Route Content -->
  <slot />
</AppShell>

<style>
  svg.buy-tickets {
    height: 25px;
    width: auto;
    fill: currentColor;
    vertical-align: middle;
  }
</style>
