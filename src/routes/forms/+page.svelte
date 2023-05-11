<script>
  import { forms } from "$lib/Forms/forms";
</script>

<section class="hero">
  <h1 class="font-bold text-center pt-10">2023 Forms</h1>
  <div class="max-w-screen-xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 xl:grid-cols-4 gap-4">
      {#each forms as form}
        <a href="pdf/{form.link}.pdf" target="_blank" rel="noopener noreferrer" class="card rounded-lg shadow-sm hover:shadow-lg outline outline-white">
          <div class="px-4 py-4 sm:px-6">
            <h2 class="text-lg font-medium">{form.title}</h2>
          </div>
          <div class="border-t border-gray-200 px-4 py-4 sm:px-6">
            <div class="flex items-center text-sm font-medium text-gray-500">
              <svg viewBox="0 0 48 48" fill="currentColor">
                <use xlink:href="#icon-document"></use>
              </svg>
              <div>Download</div>
            </div>
          </div>
        </a>
      {/each}
    </div>
  </div>
</section>

<style>
  .hero {
    background: center / cover url('/isometric.svg'), linear-gradient(to bottom right, red, maroon);
		background-blend-mode: darken;
  }
  .hero div div {
    font-size: clamp(0.5rem, 5vw, 2rem);
  }
  svg {
  height: 30px;
  width: auto;
  vertical-align: bottom;
	margin-right: 10px;
	}
</style>
