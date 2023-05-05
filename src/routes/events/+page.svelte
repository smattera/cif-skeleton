<script>
	import { fairDates } from '$lib/Schedule/fairDates';
	import { day01events } from '$lib/Schedule/day01Events';
	import { Tab, TabGroup } from '@skeletonlabs/skeleton';

	let tabSet = 0;
</script>

<section class="hero bg-section flex flex-col">
	<img src="/img/event-banner.webp" alt="Events" class="hidden lg:inline-block p-4" />
	<img src="/img/event-banner02.webp" alt="Events" class="lg:hidden p-4" />

  
	<div class="tab-group space-y-4 flex flex-col" data-testid="tab-group">
		<div
			class="tab-list flex justify-center"
			role="tablist"
			aria-labelledby=""
		>
			<label
				><div
					class="tab text-center cursor-pointer transition-colors duration-100 flex-none px-4 py-2 rounded-lg variant-filled-primary"
					data-testid="tab"
					role="tab"
					aria-controls=""
					aria-selected="true"
					tabindex="0"
				>
					<div class="h-0 w-0 overflow-hidden">
						<input type="radio" name="tab05" value="0" tabindex="-1" />
					</div>
					<div class="tab-interface space-y-1">
						<div class="tab-label">
							<span class="text-2xl s-N-9Ekhs3dG6k">Wed</span><br class="s-N-9Ekhs3dG6k" />
							<span class="text-2xl s-N-9Ekhs3dG6k">Jul</span><br class="s-N-9Ekhs3dG6k" />
							<span class="text-5xl s-N-9Ekhs3dG6k">05</span>
						</div>
					</div>
				</div></label
			><label
				><div
					class="tab text-center cursor-pointer transition-colors duration-100 flex-none px-4 py-2 rounded-lg hover:variant-soft-primary"
					data-testid="tab"
					role="tab"
					aria-controls=""
					aria-selected="false"
					tabindex="0"
				>
					<div class="h-0 w-0 overflow-hidden">
						<input type="radio" name="tab06" value="1" tabindex="-1" />
					</div>
					<div class="tab-interface space-y-1">
						<div class="tab-label">
							<span class="text-2xl s-N-9Ekhs3dG6k">Thu</span><br class="s-N-9Ekhs3dG6k" />
							<span class="text-2xl s-N-9Ekhs3dG6k">Jul</span><br class="s-N-9Ekhs3dG6k" />
							<span class="text-5xl s-N-9Ekhs3dG6k">06</span>
						</div>
					</div>
				</div></label
			><label
				><div
					class="tab text-center cursor-pointer transition-colors duration-100 flex-none px-4 py-2 rounded-lg hover:variant-soft-primary"
					data-testid="tab"
					role="tab"
					aria-controls=""
					aria-selected="false"
					tabindex="0"
				>
					<div class="h-0 w-0 overflow-hidden">
						<input type="radio" name="tab07" value="2" tabindex="-1" />
					</div>
					<div class="tab-interface space-y-1">
						<div class="tab-label">
							<span class="text-2xl s-N-9Ekhs3dG6k">Fri</span><br class="s-N-9Ekhs3dG6k" />
							<span class="text-2xl s-N-9Ekhs3dG6k">Jul</span><br class="s-N-9Ekhs3dG6k" />
							<span class="text-5xl s-N-9Ekhs3dG6k">07</span>
						</div>
					</div>
				</div></label
			><label
				><div
					class="tab text-center cursor-pointer transition-colors duration-100 flex-none px-4 py-2 rounded-lg hover:variant-soft-primary"
					data-testid="tab"
					role="tab"
					aria-controls=""
					aria-selected="false"
					tabindex="0"
				>
					<div class="h-0 w-0 overflow-hidden">
						<input type="radio" name="tab08" value="3" tabindex="-1" />
					</div>
					<div class="tab-interface space-y-1">
						<div class="tab-label">
							<span class="text-2xl s-N-9Ekhs3dG6k">Sat</span><br class="s-N-9Ekhs3dG6k" />
							<span class="text-2xl s-N-9Ekhs3dG6k">Jul</span><br class="s-N-9Ekhs3dG6k" />
							<span class="text-5xl s-N-9Ekhs3dG6k">08</span>
						</div>
					</div>
				</div></label
			><label
				><div
					class="tab text-center cursor-pointer transition-colors duration-100 flex-none px-4 py-2 rounded-lg hover:variant-soft-primary"
					data-testid="tab"
					role="tab"
					aria-controls=""
					aria-selected="false"
					tabindex="0"
				>
					<div class="h-0 w-0 overflow-hidden">
						<input type="radio" name="tab10" value="4" tabindex="-1" />
					</div>
					<div class="tab-interface space-y-1">
						<div class="tab-label">
							<span class="text-2xl s-N-9Ekhs3dG6k">Mon</span><br class="s-N-9Ekhs3dG6k" />
							<span class="text-2xl s-N-9Ekhs3dG6k">Jul</span><br class="s-N-9Ekhs3dG6k" />
							<span class="text-5xl s-N-9Ekhs3dG6k">10</span>
						</div>
					</div>
				</div></label
			><label
				><div
					class="tab text-center cursor-pointer transition-colors duration-100 flex-none px-4 py-2 rounded-lg hover:variant-soft-primary"
					data-testid="tab"
					role="tab"
					aria-controls=""
					aria-selected="false"
					tabindex="0"
				>
					<div class="h-0 w-0 overflow-hidden">
						<input type="radio" name="tab11" value="5" tabindex="-1" />
					</div>
					<div class="tab-interface space-y-1">
						<div class="tab-label">
							<span class="text-2xl s-N-9Ekhs3dG6k">Tue</span><br class="s-N-9Ekhs3dG6k" />
							<span class="text-2xl s-N-9Ekhs3dG6k">Jul</span><br class="s-N-9Ekhs3dG6k" />
							<span class="text-5xl s-N-9Ekhs3dG6k">11</span>
						</div>
					</div>
				</div></label
			><label
				><div
					class="tab text-center cursor-pointer transition-colors duration-100 flex-none px-4 py-2 rounded-lg hover:variant-soft-primary"
					data-testid="tab"
					role="tab"
					aria-controls=""
					aria-selected="false"
					tabindex="0"
				>
					<div class="h-0 w-0 overflow-hidden">
						<input type="radio" name="tab12" value="6" tabindex="-1" />
					</div>
					<div class="tab-interface space-y-1">
						<div class="tab-label">
							<span class="text-2xl s-N-9Ekhs3dG6k">Wed</span><br class="s-N-9Ekhs3dG6k" />
							<span class="text-2xl s-N-9Ekhs3dG6k">Jul</span><br class="s-N-9Ekhs3dG6k" />
							<span class="text-5xl s-N-9Ekhs3dG6k">12</span>
						</div>
					</div>
				</div></label
			><label
				><div
					class="tab text-center cursor-pointer transition-colors duration-100 flex-none px-4 py-2 rounded-lg hover:variant-soft-primary"
					data-testid="tab"
					role="tab"
					aria-controls=""
					aria-selected="false"
					tabindex="0"
				>
					<div class="h-0 w-0 overflow-hidden">
						<input type="radio" name="tab13" value="7" tabindex="-1" />
					</div>
					<div class="tab-interface space-y-1">
						<div class="tab-label">
							<span class="text-2xl s-N-9Ekhs3dG6k">Thu</span><br class="s-N-9Ekhs3dG6k" />
							<span class="text-2xl s-N-9Ekhs3dG6k">Jul</span><br class="s-N-9Ekhs3dG6k" />
							<span class="text-5xl s-N-9Ekhs3dG6k">13</span>
						</div>
					</div>
				</div></label
			><label
				><div
					class="tab text-center cursor-pointer transition-colors duration-100 flex-none px-4 py-2 rounded-lg hover:variant-soft-primary"
					data-testid="tab"
					role="tab"
					aria-controls=""
					aria-selected="false"
					tabindex="0"
				>
					<div class="h-0 w-0 overflow-hidden">
						<input type="radio" name="tab14" value="8" tabindex="-1" />
					</div>
					<div class="tab-interface space-y-1">
						<div class="tab-label">
							<span class="text-2xl s-N-9Ekhs3dG6k">Fri</span><br class="s-N-9Ekhs3dG6k" />
							<span class="text-2xl s-N-9Ekhs3dG6k">Jul</span><br class="s-N-9Ekhs3dG6k" />
							<span class="text-5xl s-N-9Ekhs3dG6k">14</span>
						</div>
					</div>
				</div></label
			><label
				><div
					class="tab text-center cursor-pointer transition-colors duration-100 flex-none px-4 py-2 rounded-lg hover:variant-soft-primary"
					data-testid="tab"
					role="tab"
					aria-controls=""
					aria-selected="false"
					tabindex="0"
				>
					<div class="h-0 w-0 overflow-hidden">
						<input type="radio" name="tab15" value="9" tabindex="-1" />
					</div>
					<div class="tab-interface space-y-1">
						<div class="tab-label">
							<span class="text-2xl s-N-9Ekhs3dG6k">Sat</span><br class="s-N-9Ekhs3dG6k" />
							<span class="text-2xl s-N-9Ekhs3dG6k">Jul</span><br class="s-N-9Ekhs3dG6k" />
							<span class="text-5xl s-N-9Ekhs3dG6k">15</span>
						</div>
					</div>
				</div></label
			>
		</div>
		<div class="tab-panel" role="tabpanel" aria-labelledby="">
			<div
				class="grid grid-cols-2 md:grid-cols-4 gap-4 p-8 my-8 w-11/12 mx-auto bg-surface-700 rounded-lg outline outline-white s-N-9Ekhs3dG6k"
			>
				<div class="text-3xl s-N-9Ekhs3dG6k">6:00 PM</div>
				<div class="col-span-2 s-N-9Ekhs3dG6k">
					<a href="/stickball" class="decoration-transparent s-N-9Ekhs3dG6k"
						><span class="chip variant-filled-success s-N-9Ekhs3dG6k">Stickball</span><br
							class="s-N-9Ekhs3dG6k"
						/></a
					> Opening Ceremonies, Fallen Tushka Ceremony, &amp; Happy Feet Social Dancers
				</div>
				<div class="col-span-2 md:col-span-1 s-N-9Ekhs3dG6k">Warrior Stadium</div>
				<hr class="col-span-2 md:col-span-4 s-N-9Ekhs3dG6k" />
				<div class="text-3xl s-N-9Ekhs3dG6k">7:00 PM</div>
				<div class="col-span-2 s-N-9Ekhs3dG6k">
					<a href="/stickball" class="decoration-transparent s-N-9Ekhs3dG6k"
						><span class="chip variant-filled-success s-N-9Ekhs3dG6k">Stickball</span><br
							class="s-N-9Ekhs3dG6k"
						/></a
					> Alla Tik Tóli (14-17) Exhibition Game
				</div>
				<div class="col-span-2 md:col-span-1 s-N-9Ekhs3dG6k">Warrior Stadium</div>
				<hr class="col-span-2 md:col-span-4 s-N-9Ekhs3dG6k" />
				<div class="text-3xl s-N-9Ekhs3dG6k">8:00 PM</div>
				<div class="col-span-2 s-N-9Ekhs3dG6k">
					<a href="/stickball" class="decoration-transparent s-N-9Ekhs3dG6k"
						><span class="chip variant-filled-success s-N-9Ekhs3dG6k">Stickball</span><br
							class="s-N-9Ekhs3dG6k"
						/></a
					> Legends: Men's (50+) Exhibition Game: North VS South
				</div>
				<div class="col-span-2 md:col-span-1 s-N-9Ekhs3dG6k">Warrior Stadium</div>
				<hr class="col-span-2 md:col-span-4 s-N-9Ekhs3dG6k" />
				<div class="text-3xl s-N-9Ekhs3dG6k">9:00 PM</div>
				<div class="col-span-2 s-N-9Ekhs3dG6k">
					<a href="/stickball" class="decoration-transparent s-N-9Ekhs3dG6k"
						><span class="chip variant-filled-success s-N-9Ekhs3dG6k">Stickball</span><br
							class="s-N-9Ekhs3dG6k"
						/></a
					> Women's (35+) Exhibition Game: North VS South
				</div>
				<div class="col-span-2 md:col-span-1 s-N-9Ekhs3dG6k">Warrior Stadium</div>
				<hr class="col-span-2 md:col-span-4 s-N-9Ekhs3dG6k" />
				<div class="text-3xl s-N-9Ekhs3dG6k">10:00 PM</div>
				<div class="col-span-2 s-N-9Ekhs3dG6k">
					<a href="/stickball" class="decoration-transparent s-N-9Ekhs3dG6k"
						><span class="chip variant-filled-success s-N-9Ekhs3dG6k">Stickball</span><br
							class="s-N-9Ekhs3dG6k"
						/></a
					> Men's Division: Game 1
				</div>
				<div class="col-span-2 md:col-span-1 s-N-9Ekhs3dG6k">Warrior Stadium</div>
				<hr class="col-span-2 md:col-span-4 s-N-9Ekhs3dG6k" />
				<div class="col-span-2 md:col-span-4 italic text-center s-N-9Ekhs3dG6k">End of day</div>
			</div>
		</div>
	</div>

	<TabGroup
		class="flex flex-col"
		justify="justify-center"
		active="variant-filled-primary"
		hover="hover:variant-soft-primary"
		rounded="rounded-lg"
		border=""
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
							{#if event.category === 'culture'}
								<a href="/culture" class="decoration-transparent">
									<span class="chip variant-filled-secondary">Culture</span><br />
								</a>
							{:else if event.category === 'family'}
								<a href="/family" class="decoration-transparent">
									<span class="chip variant-filled-tertiary">Family Fun</span><br />
								</a>
							{:else if event.category === 'stickball'}
								<a href="/stickball" class="decoration-transparent">
									<span class="chip variant-filled-success">Stickball</span><br />
								</a>
							{:else if event.category === 'pageant'}
								<a href="/pageant" class="decoration-transparent">
									<span class="chip variant-filled-warning">Pageant</span><br />
								</a>
							{:else if event.category === 'competitions'}
								<a href="/competitions" class="decoration-transparent">
									<span class="chip variant-filled-error">Competitions</span><br />
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
							{#if event.category === 'culture'}
								<a href="/culture" class="decoration-transparent">
									<span class="chip variant-filled-secondary">Culture</span><br />
								</a>
							{:else if event.category === 'family'}
								<a href="/family" class="decoration-transparent">
									<span class="chip variant-filled-tertiary">Family Fun</span><br />
								</a>
							{:else if event.category === 'stickball'}
								<a href="/stickball" class="decoration-transparent">
									<span class="chip variant-filled-success">Stickball</span><br />
								</a>
							{:else if event.category === 'pageant'}
								<a href="/pageant" class="decoration-transparent">
									<span class="chip variant-filled-warning">Pageant</span><br />
								</a>
							{:else if event.category === 'competitions'}
								<a href="/competitions" class="decoration-transparent">
									<span class="chip variant-filled-error">Competitions</span><br />
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
							{#if event.category === 'culture'}
								<a href="/culture" class="decoration-transparent">
									<span class="chip variant-filled-secondary">Culture</span><br />
								</a>
							{:else if event.category === 'family'}
								<a href="/family" class="decoration-transparent">
									<span class="chip variant-filled-tertiary">Family Fun</span><br />
								</a>
							{:else if event.category === 'stickball'}
								<a href="/stickball" class="decoration-transparent">
									<span class="chip variant-filled-success">Stickball</span><br />
								</a>
							{:else if event.category === 'pageant'}
								<a href="/pageant" class="decoration-transparent">
									<span class="chip variant-filled-warning">Pageant</span><br />
								</a>
							{:else if event.category === 'competitions'}
								<a href="/competitions" class="decoration-transparent">
									<span class="chip variant-filled-error">Competitions</span><br />
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
							{#if event.category === 'culture'}
								<a href="/culture" class="decoration-transparent">
									<span class="chip variant-filled-secondary">Culture</span><br />
								</a>
							{:else if event.category === 'family'}
								<a href="/family" class="decoration-transparent">
									<span class="chip variant-filled-tertiary">Family Fun</span><br />
								</a>
							{:else if event.category === 'stickball'}
								<a href="/stickball" class="decoration-transparent">
									<span class="chip variant-filled-success">Stickball</span><br />
								</a>
							{:else if event.category === 'pageant'}
								<a href="/pageant" class="decoration-transparent">
									<span class="chip variant-filled-warning">Pageant</span><br />
								</a>
							{:else if event.category === 'competitions'}
								<a href="/competitions" class="decoration-transparent">
									<span class="chip variant-filled-error">Competitions</span><br />
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
							{#if event.category === 'culture'}
								<a href="/culture" class="decoration-transparent">
									<span class="chip variant-filled-secondary">Culture</span><br />
								</a>
							{:else if event.category === 'family'}
								<a href="/family" class="decoration-transparent">
									<span class="chip variant-filled-tertiary">Family Fun</span><br />
								</a>
							{:else if event.category === 'stickball'}
								<a href="/stickball" class="decoration-transparent">
									<span class="chip variant-filled-success">Stickball</span><br />
								</a>
							{:else if event.category === 'pageant'}
								<a href="/pageant" class="decoration-transparent">
									<span class="chip variant-filled-warning">Pageant</span><br />
								</a>
							{:else if event.category === 'competitions'}
								<a href="/competitions" class="decoration-transparent">
									<span class="chip variant-filled-error">Competitions</span><br />
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
							{#if event.category === 'culture'}
								<a href="/culture" class="decoration-transparent">
									<span class="chip variant-filled-secondary">Culture</span><br />
								</a>
							{:else if event.category === 'family'}
								<a href="/family" class="decoration-transparent">
									<span class="chip variant-filled-tertiary">Family Fun</span><br />
								</a>
							{:else if event.category === 'stickball'}
								<a href="/stickball" class="decoration-transparent">
									<span class="chip variant-filled-success">Stickball</span><br />
								</a>
							{:else if event.category === 'pageant'}
								<a href="/pageant" class="decoration-transparent">
									<span class="chip variant-filled-warning">Pageant</span><br />
								</a>
							{:else if event.category === 'competitions'}
								<a href="/competitions" class="decoration-transparent">
									<span class="chip variant-filled-error">Competitions</span><br />
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
							{#if event.category === 'culture'}
								<a href="/culture" class="decoration-transparent">
									<span class="chip variant-filled-secondary">Culture</span><br />
								</a>
							{:else if event.category === 'family'}
								<a href="/family" class="decoration-transparent">
									<span class="chip variant-filled-tertiary">Family Fun</span><br />
								</a>
							{:else if event.category === 'stickball'}
								<a href="/stickball" class="decoration-transparent">
									<span class="chip variant-filled-success">Stickball</span><br />
								</a>
							{:else if event.category === 'pageant'}
								<a href="/pageant" class="decoration-transparent">
									<span class="chip variant-filled-warning">Pageant</span><br />
								</a>
							{:else if event.category === 'competitions'}
								<a href="/competitions" class="decoration-transparent">
									<span class="chip variant-filled-error">Competitions</span><br />
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
							{#if event.category === 'culture'}
								<a href="/culture" class="decoration-transparent">
									<span class="chip variant-filled-secondary">Culture</span><br />
								</a>
							{:else if event.category === 'family'}
								<a href="/family" class="decoration-transparent">
									<span class="chip variant-filled-tertiary">Family Fun</span><br />
								</a>
							{:else if event.category === 'stickball'}
								<a href="/stickball" class="decoration-transparent">
									<span class="chip variant-filled-success">Stickball</span><br />
								</a>
							{:else if event.category === 'pageant'}
								<a href="/pageant" class="decoration-transparent">
									<span class="chip variant-filled-warning">Pageant</span><br />
								</a>
							{:else if event.category === 'competitions'}
								<a href="/competitions" class="decoration-transparent">
									<span class="chip variant-filled-error">Competitions</span><br />
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
							{#if event.category === 'culture'}
								<a href="/culture" class="decoration-transparent">
									<span class="chip variant-filled-secondary">Culture</span><br />
								</a>
							{:else if event.category === 'family'}
								<a href="/family" class="decoration-transparent">
									<span class="chip variant-filled-tertiary">Family Fun</span><br />
								</a>
							{:else if event.category === 'stickball'}
								<a href="/stickball" class="decoration-transparent">
									<span class="chip variant-filled-success">Stickball</span><br />
								</a>
							{:else if event.category === 'pageant'}
								<a href="/pageant" class="decoration-transparent">
									<span class="chip variant-filled-warning">Pageant</span><br />
								</a>
							{:else if event.category === 'competitions'}
								<a href="/competitions" class="decoration-transparent">
									<span class="chip variant-filled-error">Competitions</span><br />
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
							{#if event.category === 'culture'}
								<a href="/culture" class="decoration-transparent">
									<span class="chip variant-filled-secondary">Culture</span><br />
								</a>
							{:else if event.category === 'family'}
								<a href="/family" class="decoration-transparent">
									<span class="chip variant-filled-tertiary">Family Fun</span><br />
								</a>
							{:else if event.category === 'stickball'}
								<a href="/stickball" class="decoration-transparent">
									<span class="chip variant-filled-success">Stickball</span><br />
								</a>
							{:else if event.category === 'pageant'}
								<a href="/pageant" class="decoration-transparent">
									<span class="chip variant-filled-warning">Pageant</span><br />
								</a>
							{:else if event.category === 'competitions'}
								<a href="/competitions" class="decoration-transparent">
									<span class="chip variant-filled-error">Competitions</span><br />
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
