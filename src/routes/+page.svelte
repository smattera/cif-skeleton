<script>
	import Countdown from "../components/Countdown.svelte";
</script>

<svelte:head>
	<title>Choctaw Indian Fair | Home</title>
</svelte:head>

<video autoplay loop muted playsinline class="relative top-0 left-0 w-full object-cover -z-[1] h-[75vh]" poster="./img/CIF-bg.webp">
	<source src="./vid/CIFVideoWeb.mp4" type="video/mp4"/>
</video>

<Countdown />

<section class="flex flex-col md:flex-row items-center py-12 px-4">
  <div class="md:w-1/2 md:pr-8 max-w-7xl">
    <img src="/img/chiefprincess.webp" alt="Chief & Princess" class="rounded-lg shadow-lg"/>
  </div>
  <div class="md:w-1/2 text-center pt-10 md:pt-0">
		<h1><span class="gradient-heading">Halito!</span></h1>
    <h1 class="text-4xl md:text-5xl font-bold leading-tight mb-4">
      Welcome to My Website
    </h1>
    <p class="text-lg md:text-xl mb-8">
      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolores, atque nobis voluptate tempora numquam velit doloribus nam quos et perferendis esse repellat excepturi deserunt vero quia? Quidem natus facere ea.
    </p>
    <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full">
      Get Started
    </button>
  </div>
</section>

<style>
	section {
    background: center / cover url('/isometric.svg'), linear-gradient(to bottom right, red, maroon);
		background-blend-mode: darken;
  }
	.gradient-heading {
		font-size: 4rem;
		font-weight: 600;
		@apply bg-clip-text text-transparent box-decoration-clone;
		/* Direction */
		@apply bg-gradient-to-br;
		/* Color Stops */
		@apply from-primary-500 via-surface-50 to-primary-600;
	}
</style>
