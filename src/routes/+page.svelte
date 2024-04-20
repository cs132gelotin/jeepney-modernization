<script lang="ts">
	import { onMount } from 'svelte';
	import Autoplay from 'embla-carousel-autoplay';
	import * as Carousel from '$lib/components/ui/carousel/index.js';
	import * as Card from '$lib/components/ui/card';
	import Navigation from '$lib/Navigation.svelte';
	import jeep1 from '$lib/assets/jeep1.jpg';

	let theme: string;
	// On component mount
	onMount(() => {
		// Check if the html element has the class 'dark'
		theme = document.documentElement.classList.contains('dark') ? 'dark' : 'light';
	});

	const plugin = Autoplay({ delay: 3000, stopOnInteraction: true });
</script>

<Navigation></Navigation>
<main>
	<section
		class="mx-auto flex h-full max-w-6xl flex-col items-center justify-center gap-2 py-16 text-center"
	>
		<h1 class="leading-1.1 text-6xl font-bold tracking-tighter">
			#Jeepney<span class="text-muted">Moder</span>N<span class="text-muted">iz</span>ation
		</h1>
		<h1 class="leading-1.1 text-5xl font-bold tracking-tighter text-primary">
			Sentiments on Modernization
		</h1>
		<p class="mb-6 max-w-[750px] text-lg text-muted-foreground">
			A Twitter analysis of Filipino reception towards Jeepney Modernization
		</p>
		<Carousel.Root
			class="w-full max-w-2xl"
			plugins={[plugin]}
			on:mouseenter={plugin.stop}
			on:mouseleave={plugin.reset}
		>
			<Carousel.Content>
				{#each Array(5) as _, i (i)}
					<Carousel.Item>
						<div class="p-1">
							<Card.Root>
								<Card.Content class="flex items-center justify-center p-6">
									<blockquote class="twitter-tweet" data-theme={theme}>
										<p lang="en" dir="ltr">
											Sara, Arjo, etc. don’t get it: among all people, it’s the jeepney drivers who
											will suffer the most, because no income for 7 days. But the move is drastic
											because their calls remain unheeded and their concerns, unaddressed. Grabe
											yung kakulangan ng pang unawa sa gubyernong ito.
										</p>
										&mdash; Claudiopoi #StopKillingPalestinians!!! 🇵🇸 (@claudiopoy)<a
											href="https://twitter.com/claudiopoy/status/1632356980601032705?ref_src=twsrc%5Etfw"
											>March 5, 2023</a
										>
									</blockquote>
									<script
										async
										src="https://platform.twitter.com/widgets.js"
										charset="utf-8"
									></script>
								</Card.Content>
							</Card.Root>
						</div>
					</Carousel.Item>
				{/each}
			</Carousel.Content>
			<Carousel.Previous />
			<Carousel.Next />
		</Carousel.Root>
	</section>
	<section
		class="mx-auto flex max-w-6xl flex-col items-center justify-center gap-2 py-20 text-center"
	>
		<p class="max-w-[850px] text-2xl leading-7 [&:not(:first-child)]:mt-6">
			Our project,
			<span class="font-bold underline decoration-sky-500 decoration-4"
				>Twitter Analysis on the PUV Modernization Program</span
			>, aims to study Twitter data related to the issue regarding the PUV Modernization Program. It
			attempts to analyze and understand the general opinion and perspective of people about the PUV
			Modernization Program.
		</p>
	</section>

	<section class="mx-auto grid max-w-6xl grid-cols-2 items-center gap-16 px-4 py-20" id="Overview">
		<div>
			<h1 class="text-7xl font-extrabold tracking-tight">01</h1>
			<h1 class="text-4xl font-extrabold tracking-tight">Overview</h1>
			<p class="mt-6">
				The PUV Modernization Program has been one of the relevant issues in the Philippines. Not
				only has it affected PUV drivers, but also commuters which encompasses the majority of the
				people. Numerous strikes were held in hopes of the government and drivers to have an
				agreement regarding this, which affected commuters. With this, we have decided to study the
				general reaction of the people regarding the issue which can provide insights on how the
				program is perceived by them.
			</p>
		</div>
		<div class="relative h-full">
			<img
				class="h-full w-full rounded-lg object-cover"
				src={jeep1}
				alt="#NoToJeepneyPhaseout Rally"
			/>
		</div>
	</section>

	<section class="mx-auto flex max-w-6xl flex-col gap-6 px-4 py-20" id="Problem">
		<div>
			<h1 class="text-7xl font-extrabold tracking-tight">02</h1>
			<h1 class="text-4xl font-extrabold tracking-tight">Problem</h1>
		</div>
		<div class="grid grid-cols-5 grid-rows-3 gap-8">
			<div
				class="col-span-3 row-span-2 rounded-3xl bg-secondary p-8 duration-100 ease-in hover:bg-primary hover:text-white"
			>
				<h2 class="scroll-m-20 pb-2 text-3xl font-semibold tracking-tight">Research Question</h2>
				<p class="leading-7 [&:not(:first-child)]:mt-6">
					What is the general attitude of the population regarding the PUV Modernization Program?
				</p>
			</div>
			<div
				class="col-span-2 rounded-3xl bg-secondary p-8 duration-100 ease-in hover:bg-primary hover:text-white"
			>
				<h3 class="scroll-m-20 text-2xl font-semibold tracking-tight">Null Hypothesis</h3>
				<p class="leading-7 [&:not(:first-child)]:mt-6">
					There is no significant difference in the attitude of the population about the PUV
					Modernization Program.
				</p>
			</div>
			<div
				class="col-span-2 rounded-3xl bg-secondary p-8 duration-100 ease-in hover:bg-primary hover:text-white"
			>
				<h3 class="scroll-m-20 text-2xl font-semibold tracking-tight">Alternative Hypothesis</h3>
				<p class="leading-7 [&:not(:first-child)]:mt-6">
					There is a significant difference in the attitude of the population about the PUV
					Modernization Program.
				</p>
			</div>
			<div
				class="col-span-5 rounded-3xl bg-secondary p-8 duration-100 ease-in hover:bg-primary hover:text-white"
			>
				<h2 class="scroll-m-20 pb-2 text-3xl font-semibold tracking-tight">Solution</h2>
				<p class="leading-7 [&:not(:first-child)]:mt-6">
					Analyze tweets related to the PUV Modernization Program
				</p>
			</div>
		</div>
	</section>
	<section class="mx-auto flex max-w-6xl flex-col gap-6 px-4 py-20" id="DataCollection">
		<div>
			<h1 class="text-7xl font-extrabold tracking-tight">03</h1>
			<h1 class="text-4xl font-extrabold tracking-tight">Data Collection</h1>
		</div>
		<div class="grid grid-cols-6 grid-rows-3 gap-8">
			<div
				class="col-span-2 row-span-2 rounded-3xl bg-secondary p-8 duration-100 ease-in hover:bg-primary hover:text-white"
			>
				<h2 class="scroll-m-20 text-3xl font-semibold tracking-tight">Collection</h2>
				<p class="leading-7 [&:not(:first-child)]:mt-6">
					Due to recent modifications to X/Twitter's API, the data collection tool SNScrape has
					exhibited limitations in retrieving data effectively. To ensure the integrity of our
					project, we employed a manual Twitter scraping approach targeting a minimum of 1000 tweets
					from 2022 to the present (2024) encompassing keywords directly relevant to the research
					topic.
				</p>
			</div>
			<div
				class="col-span-2 row-span-2 rounded-3xl bg-secondary p-8 duration-100 ease-in hover:bg-primary hover:text-white"
			>
				<h3 class="scroll-m-20 text-3xl font-semibold tracking-tight">Pre-processing</h3>
				<p class="leading-7 [&:not(:first-child)]:mt-6">
					Collected tweets underwent rigorous pre-processing to ensure quality. This includes
					removing duplicates, non-text content, and formatting inconsistencies. The pre-processed
					data also underwent validation checks to ensure consistency and adherence to the defined
					criteria for inclusion.
				</p>
			</div>
			<div
				class="col-span-2 row-span-2 rounded-3xl bg-secondary p-8 duration-100 ease-in hover:bg-primary hover:text-white"
			>
				<h3 class="scroll-m-20 text-3xl font-semibold tracking-tight">Exploration</h3>
				<p class="leading-7 [&:not(:first-child)]:mt-6">
					After collection and pre-processing, the data will undergo exploratory analysis to gain
					insights into tweet content, distribution of keywords, and potential presence of outliers.
					This initial exploration will inform subsequent data cleaning and analysis strategies.
				</p>
			</div>
			<div
				class="col-span-6 flex items-center rounded-3xl bg-secondary p-8 duration-100 ease-in hover:bg-primary hover:text-white"
			>
				<h2 class="scroll-m-20 text-3xl font-semibold tracking-tight">Keywords</h2>
			</div>
		</div>
	</section>
</main>
