<script lang="ts">
	import { onMount } from 'svelte';
	import Autoplay from 'embla-carousel-autoplay';
	import * as Carousel from '$lib/components/ui/carousel/index.js';
	import * as Card from '$lib/components/ui/card';
	import * as HoverCard from '$lib/components/ui/hover-card/index.js';
	import * as Avatar from '$lib/components/ui/avatar/index.js';
	import { Button } from '$lib/components/ui/button/index.js';
	import { buttonVariants } from '$lib/components/ui/button';
	import Navigation from '$lib/Navigation.svelte';
	import jeep1 from '$lib/assets/jeep1.jpg';
	import GCAvatar from '$lib/assets/_DSC3637_512x512.png';
	import ADAvatar from '$lib/assets/435194078_981985919488202_6376095500813041272_n.png';
	import JGAvatar from '$lib/assets/435201424_342404608842278_1262981411790175769_n.jpg';
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
		class="w-full bg-gradient-radial-top from-blue-300/80 to-transparent dark:from-primary/10"
	>
		<div
			class="mx-auto flex h-screen-minus-navbar max-w-6xl flex-col items-center justify-center gap-2 py-16 pt-12 text-center"
		>
			<h1 class="leading-1.1 text-6xl font-bold tracking-tighter drop-shadow-xl">
				#Jeepney<span class="text-muted line-through decoration-destructive decoration-wavy"
					>Moder</span
				>N<span class="text-muted line-through decoration-destructive decoration-wavy">iz</span
				>ation
			</h1>
			<h1 class="leading-1.1 text-5xl font-bold tracking-tighter text-primary drop-shadow-lg">
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
				<Carousel.Content class="items-center">
					<Carousel.Item>
						<Card.Root>
							<Card.Content class="flex items-center justify-center p-2"
								><blockquote class="twitter-tweet" data-theme={theme}>
									<p lang="en" dir="ltr">
										1 dysfunctional aspect of Pinoy culture is treating jeepney drivers and their
										jalopies endemic.<br /><br />In 2019, prior to pandemic, jeepneys were involved
										in 10k+ cases of crashes.<br /><br />Yet the dimwit Fink will put on hold
										transpo modernization for these bozos. Un-fucking-believable.
									</p>
									&mdash; Ronn (@PulbuRonn)<a
										href="https://twitter.com/PulbuRonn/status/1494824125893787648?ref_src=twsrc%5Etfw"
										>February 19, 2022</a
									>
								</blockquote>
								<script
									async
									src="https://platform.twitter.com/widgets.js"
									charset="utf-8"
								></script></Card.Content
							>
						</Card.Root>
					</Carousel.Item>
					<Carousel.Item>
						<Card.Root>
							<Card.Content class="flex items-center justify-center p-2">
								<blockquote class="twitter-tweet" data-theme={theme}>
									<p lang="en" dir="ltr">
										This government is pushing for jeepney phaseout and limiting window hours for
										provincial buses from 10 pm to 5 am. Such policies cater to the needs of car
										owners and not commuters.<br /><br />Kaya di kapani-paniwala na ang mga proyekto
										gaya ng PAREX at skyways ay para sa commuters.
									</p>
									&mdash; Mangingisda 🇵🇸🇵🇸🇵🇸 (@MangingisdaSays)<a
										href="https://twitter.com/MangingisdaSays/status/1516979306932875265?ref_src=twsrc%5Etfw"
										>April 21, 2022</a
									>
								</blockquote>
								<script
									async
									src="https://platform.twitter.com/widgets.js"
									charset="utf-8"
								></script>
							</Card.Content>
						</Card.Root>
					</Carousel.Item>
					<Carousel.Item>
						<Card.Root>
							<Card.Content class="flex items-center justify-center p-2">
								<blockquote class="twitter-tweet" data-theme={theme}>
									<p lang="en" dir="ltr">
										For those who opposed the jeepney modernization program especially those
										senators and to the rallying groups who demand &quot;ayuda&quot; or fare
										increase, here we are.<br /><br />If only you were all open minded.
									</p>
									&mdash; Babaylan (@amIBabaylan21)<a
										href="https://twitter.com/amIBabaylan21/status/1539760658996424704?ref_src=twsrc%5Etfw"
										>June 23, 2022</a
									>
								</blockquote>
								<script
									async
									src="https://platform.twitter.com/widgets.js"
									charset="utf-8"
								></script>
							</Card.Content>
						</Card.Root>
					</Carousel.Item>
					<Carousel.Item>
						<Card.Root>
							<Card.Content class="flex items-center justify-center p-2">
								<blockquote class="twitter-tweet" data-theme={theme}>
									<p lang="en" dir="ltr">
										puvm got to be the worst, most stupid attempt in beautifying the already broken
										transpo system in the ph. marahil hindi naman talaga modernization ang aim nito,
										but to capitalize on jeepney drivers/operators. <br /><br />no to corporate
										takeover of public transport!
										<a
											href="https://twitter.com/hashtag/NoToJeepneyPhaseout?src=hash&amp;ref_src=twsrc%5Etfw"
											>#NoToJeepneyPhaseout</a
										>
									</p>
									&mdash; ️️ ً (@sy6lo)<a
										href="https://twitter.com/sy6lo/status/1740968767411417205?ref_src=twsrc%5Etfw"
										>December 30, 2023</a
									>
								</blockquote>
								<script
									async
									src="https://platform.twitter.com/widgets.js"
									charset="utf-8"
								></script>
							</Card.Content>
						</Card.Root>
					</Carousel.Item>
					<Carousel.Item>
						<Card.Root>
							<Card.Content class="flex items-center justify-center p-2"
								><blockquote class="twitter-tweet" data-theme={theme}>
									<p lang="en" dir="ltr">
										PUV MODERNIZATION WILL BRING GREATER GOOD FOR THE GREATER NUMBER.
									</p>
									&mdash; Reggie S Gazmen (@gazmen_reggie)<a
										href="https://twitter.com/gazmen_reggie/status/1741194343539679545?ref_src=twsrc%5Etfw"
										>December 30, 2023</a
									>
								</blockquote>
								<script
									async
									src="https://platform.twitter.com/widgets.js"
									charset="utf-8"
								></script></Card.Content
							>
						</Card.Root>
					</Carousel.Item>
					<Carousel.Item>
						<Card.Root>
							<Card.Content class="flex items-center justify-center p-2"
								><blockquote class="twitter-tweet" data-theme={theme}>
									<p lang="tl" dir="ltr">
										Duterte&#39;s jeepney modernization program sobrang anti-poor niya talaga.
										Pahirapan pa sa pagaapply tapos mababaon pa sa utang ang mga driver. Hindi man
										lang inisip na sapat lang ang kinikita ng mga driver sa pangaraw-araw tapos
										mababawasan pa para lang makapagbayad. <a href="https://t.co/zNPWCGPTQs"
											>https://t.co/zNPWCGPTQs</a
										>
									</p>
									&mdash; ًderrick (@maremdior)<a
										href="https://twitter.com/maremdior/status/1495059015813906432?ref_src=twsrc%5Etfw"
										>February 19, 2022</a
									>
								</blockquote>
								<script
									async
									src="https://platform.twitter.com/widgets.js"
									charset="utf-8"
								></script></Card.Content
							>
						</Card.Root>
					</Carousel.Item>
				</Carousel.Content>
				<Carousel.Previous />
				<Carousel.Next />
			</Carousel.Root>
		</div>
	</section>
	<section
		class="mx-auto flex h-screen-minus-navbar flex-col items-center justify-center gap-2 py-20 text-center"
	>
		<div
			class="absolute z-10 h-screen-minus-navbar w-full bg-jeep2 bg-cover bg-center opacity-30 blur-sm"
		></div>

		<p
			class="z-20 max-w-[850px] text-3xl font-medium leading-tight hover:drop-shadow-2xl [&:not(:first-child)]:mt-6"
		>
			Our project,
			<span
				class="font-bold underline decoration-primary/80 decoration-4 duration-200 ease-in hover:text-primary hover:decoration-transparent dark:decoration-primary dark:hover:decoration-transparent"
				>Twitter Analysis on the PUV Modernization Program</span
			>, aims to study Twitter data related to the issue. It attempts to analyze and understand the
			general opinion and perspective of people about the PUV Modernization Program.
		</p>
	</section>

	<section
		class="mx-auto grid h-screen max-w-6xl grid-cols-2 items-center gap-16 px-4 py-20"
		id="overview"
	>
		<div>
			<h1
				class="font-jeepney text-8xl font-extrabold tracking-tight text-yellow-400 drop-shadow-md"
			>
				01
			</h1>
			<h1 class="font-jeep text-7xl uppercase tracking-tight text-pink-600 drop-shadow-lg">
				Overview
			</h1>
			<p class="mt-6 text-lg">
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

	<section
		class="w-full bg-gradient-radial from-transparent to-primary/50 dark:from-primary dark:to-transparent"
		id="problem"
	>
		<div class="mx-auto flex max-w-6xl flex-col gap-6 px-4 py-20">
			<div>
				<h1
					class="font-jeepney text-8xl font-extrabold tracking-tight text-green-600 drop-shadow-md dark:text-green-400"
				>
					02
				</h1>
				<h1
					class="font-jeep text-7xl uppercase tracking-tight text-orange-600 drop-shadow-lg dark:text-orange-500"
				>
					Problem
				</h1>
			</div>
			<div class="grid auto-rows-auto grid-cols-4 gap-8">
				<div
					class="col-span-4 row-span-2 rounded-3xl bg-secondary p-8 drop-shadow-lg duration-100 ease-in hover:bg-primary hover:text-white hover:shadow-2xl"
				>
					<h2 class="scroll-m-20 pb-2 text-3xl font-bold tracking-tight">Background</h2>
					<p class="text-lg leading-7 [&:not(:first-child)]:mt-6">
						On June 19 2017, the Department of Transportation (DOTr) issued Department Order No.
						2017-011, otherwise known as the <span class="font-semibold">
							Omnibus Guidelines on the Planning and Identification of Public Road Transportation
							Services and Franchise Issuance
						</span>
						which launched the PUVMP (Public Utility Vehicle Modernization Program).
						<HoverCard.Root>
							<HoverCard.Trigger
								href="https://ltfrb.gov.ph/puv-modernization-program/"
								target="_blank"
								rel="noreferrer noopener"
								class="font-medium underline underline-offset-4 transition-all  hover:font-bold hover:decoration-2 focus-visible:outline-black"
								>[ 1 ]</HoverCard.Trigger
							>
							<HoverCard.Content>
								<div class="flex flex-col">
									<img
										src="https://ltfrb.gov.ph/wp-content/uploads/2023/05/PUVMP-logo-1536x1027.png"
										alt="PUVMP Banner"
									/>
									<p>LTFRB | PUV Modernization Program</p>
								</div>
							</HoverCard.Content>
						</HoverCard.Root>
					</p>
					<p class="text-lg leading-7 [&:not(:first-child)]:mt-6">
						The program aims to transform the road sector of public transport through the
						introduction of safer and climate-friendly vehicles, improved regulation, and industry
						consolidation. The program is beneficial in the long run however operators are caught in
						a difficult situation due to the high cost of the program. According to the Office of
						Transportation Cooperatives, jeepney operators must raise P300,000 in paid-up capital.
						Operators may have to spend between P20,000 to P30,000 each to comply with other
						requirements. Under the Omnibus Franchising Guidelines, cooperatives and corporations
						will also be required to eventually upgrade their fleet into modern jeepneys, which can
						cost up to P2.5 million per unit.
						<HoverCard.Root>
							<HoverCard.Trigger
								href="https://changing-transport.org/modernizing-public-transport-in-the-philippines/"
								target="_blank"
								rel="noreferrer noopener"
								class="font-medium underline underline-offset-4 transition-all  hover:font-bold hover:decoration-2 focus-visible:outline-black"
								>[ 2 ]</HoverCard.Trigger
							>
							<HoverCard.Content>
								<div class="flex flex-col">
									<img
										src="https://changing-transport.org/wp-content/uploads/MicrosoftTeams-image-1024x768.jpg"
										alt="Modern Electric Jeepney"
									/>
									<p>Changing Transport | Modernizing Public Transport in the Philippines</p>
								</div>
							</HoverCard.Content>
						</HoverCard.Root>
						<HoverCard.Root>
							<HoverCard.Trigger
								href="https://www.rappler.com/business/summary-recap-transport-strike-spotlights-jeepney-modernization-issues-march-6-2023/"
								target="_blank"
								rel="noreferrer noopener"
								class="font-medium underline underline-offset-4 transition-all  hover:font-bold hover:decoration-2 focus-visible:outline-black"
								>[ 3 ]</HoverCard.Trigger
							>
							<HoverCard.Content>
								<div class="flex flex-col">
									<img
										src="https://www.rappler.com/tachyon/2023/03/jeepney-stike-puv-modernization-drivers-protest-march-6-2023-001-scaled.jpg?resize=2560%2C1707&zoom=1"
										alt="Jeepney driver with #NoToPUVPhaseout placard"
									/>
									<p>
										Rappler (Lance Yu) | ‘Welga kami!’ Transport strike spotlights jeepney
										modernization issues
									</p>
								</div>
							</HoverCard.Content>
						</HoverCard.Root>
					</p>
					<p class="text-lg leading-7 [&:not(:first-child)]:mt-6">
						The program would surely improve public transportation however, jeepney drivers and
						operators – who already subsist on low wages – must then work to pay off millions in
						debt and interest.
					</p>
				</div>
				<div
					class="col-span-1 row-span-2 rounded-3xl bg-secondary p-8 drop-shadow-lg duration-100 ease-in hover:bg-primary hover:text-white hover:shadow-2xl"
				>
					<i class="fa-regular fa-circle-question fa-2xl mb-4"></i>
					<h2 class="scroll-m-20 pb-2 text-3xl font-bold tracking-tight">Research Question</h2>
					<p class="text-lg leading-7 [&:not(:first-child)]:mt-6">
						What is the general attitude of the population regarding the PUV Modernization Program?
					</p>
				</div>
				<div
					class="group col-span-2 rounded-3xl bg-secondary p-8 drop-shadow-lg duration-100 ease-in hover:bg-primary hover:text-white hover:shadow-2xl"
				>
					<h3
						class="scroll-m-20 text-2xl font-semibold tracking-tight text-red-500 group-hover:text-red-300 dark:text-red-400"
					>
						Null Hypothesis
					</h3>
					<p class="text-lg leading-7 [&:not(:first-child)]:mt-6">
						There is no significant difference in the attitude of the population about the PUV
						Modernization Program.
					</p>
				</div>
				<div
					class="col-span-1 row-span-2 rounded-3xl bg-secondary p-8 drop-shadow-lg duration-100 ease-in hover:bg-primary hover:text-white hover:shadow-2xl"
				>
					<i class="fa-brands fa-twitter fa-2xl mb-4"></i>
					<h2 class="scroll-m-20 pb-2 text-3xl font-bold tracking-tight">Action<br />Plan</h2>
					<p class="text-lg leading-7 [&:not(:first-child)]:mt-6">
						Analyze social media sentiment through tweets to understand public opinion on the PUV
						Modernization Program.
					</p>
				</div>
				<div
					class="group col-span-2 rounded-3xl bg-secondary p-8 drop-shadow-lg duration-100 ease-in hover:bg-primary hover:text-white hover:shadow-2xl"
				>
					<h3
						class="scroll-m-20 text-2xl font-semibold tracking-tight text-green-500 group-hover:text-green-300 dark:text-green-400"
					>
						Alternative Hypothesis
					</h3>
					<p class="text-lg leading-7 [&:not(:first-child)]:mt-6">
						There is a significant difference in the attitude of the population about the PUV
						Modernization Program.
					</p>
				</div>
			</div>
		</div>
	</section>
	<section class="mx-auto flex max-w-6xl flex-col gap-6 px-4 py-20" id="materials&methods">
		<div class="flex flex-col items-end">
			<h1
				class="font-jeepney text-8xl font-extrabold tracking-tight text-violet-500 drop-shadow-md"
			>
				03
			</h1>
			<h1 class="font-jeep text-7xl uppercase tracking-tight text-green-500 drop-shadow-lg">
				Materials and Methods
			</h1>
			<a
				href="https://docs.google.com/spreadsheets/d/12IpBDpizXs0iUv-_JWSdayhhISXB46U-ikx9F7g1sbY/edit#gid=0"
				target="_blank"
				rel="noreferrer noopener"
				class={buttonVariants({ variant: 'outline' })}
				><i class="fa-solid fa-up-right-from-square mr-2"></i>
				<p class="">Explore the dataset here</p></a
			>
		</div>
		<div class="grid auto-rows-auto grid-cols-6 gap-8">
			<div
				class="col-span-2 row-span-1 rounded-3xl bg-secondary p-8 drop-shadow-lg duration-100 ease-in hover:bg-primary hover:text-white hover:shadow-2xl"
			>
				<i class="fa-solid fa-magnifying-glass fa-2xl mb-4"></i>
				<h2 class="scroll-m-20 text-3xl font-semibold tracking-tight">Collection</h2>
				<p class="text-lg leading-7 [&:not(:first-child)]:mt-6">
					Due to recent modifications to X/Twitter's API, the data collection tool SNScrape has
					exhibited limitations in retrieving data effectively. So instead, we employed a manual
					Twitter scraping approach targeting a minimum of 1000 tweets from 2022 to the present
					(2024) encompassing keywords directly relevant to the research topic.
				</p>
			</div>
			<div
				class="col-span-2 row-span-1 rounded-3xl bg-secondary p-8 drop-shadow-lg duration-100 ease-in hover:bg-primary hover:text-white hover:shadow-2xl"
			>
				<i class="fa-solid fa-wand-magic-sparkles fa-2xl mb-4"></i>
				<h3 class="scroll-m-20 text-3xl font-semibold tracking-tight">Pre-processing</h3>
				<p class="text-lg leading-7 [&:not(:first-child)]:mt-6">
					Collected tweets underwent rigorous pre-processing to ensure quality. This includes
					removing duplicates, non-text content, and formatting inconsistencies. The pre-processed
					data also underwent validation checks to ensure consistency and adherence to the defined
					criteria for inclusion.
				</p>
			</div>
			<div
				class="col-span-2 row-span-1 rounded-3xl bg-secondary p-8 drop-shadow-lg duration-100 ease-in hover:bg-primary hover:text-white hover:shadow-2xl"
			>
				<i class="fa-solid fa-chart-line fa-2xl mb-4"></i>
				<h3 class="scroll-m-20 text-3xl font-semibold tracking-tight">Exploration</h3>
				<p class="text-lg leading-7 [&:not(:first-child)]:mt-6">
					After collection and pre-processing, the data will undergo exploratory analysis to gain
					insights into tweet content, distribution of keywords, and potential presence of outliers.
					This initial exploration will inform subsequent data cleaning and analysis strategies.
				</p>
			</div>
			<div
				class="group col-span-6 flex flex-col items-center gap-4 rounded-3xl bg-secondary p-8 drop-shadow-lg duration-100 ease-in hover:bg-jeep3 bg-cover bg-bottom hover:shadow-2xl"
			>
				<h2 class="scroll-m-20 pb-3 text-4xl font-bold tracking-tight group-hover:text-white ">
					Keywords
				</h2>
				<div class="flex max-w-4xl flex-wrap items-center justify-center gap-x-4 gap-y-3">
					<button
						class="rounded-full bg-zinc-900 px-6 py-3 text-lg font-semibold text-white shadow-md shadow-black/50 duration-200 ease-in hover:scale-110 hover:bg-white hover:text-primary hover:shadow-lg hover:shadow-black/80"
						>electric</button
					>
					<button
						class="rounded-full bg-zinc-900 px-6 py-3 text-lg font-semibold text-white shadow-md shadow-black/50 duration-200 ease-in hover:scale-110 hover:bg-white hover:text-primary hover:shadow-lg hover:shadow-black/80"
						>jeep</button
					>
					<button
						class="rounded-full bg-zinc-900 px-6 py-3 text-lg font-semibold text-white shadow-md shadow-black/50 duration-200 ease-in hover:scale-110 hover:bg-white hover:text-primary hover:shadow-lg hover:shadow-black/80"
						>jeepney</button
					>
					<button
						class="rounded-full bg-zinc-900 px-6 py-3 text-lg font-semibold text-white shadow-md shadow-black/50 duration-200 ease-in hover:scale-110 hover:bg-white hover:text-primary hover:shadow-lg hover:shadow-black/80"
						>jeepney modernization</button
					>
					<button
						class="rounded-full bg-zinc-900 px-6 py-3 text-lg font-semibold text-white shadow-md shadow-black/50 duration-200 ease-in hover:scale-110 hover:bg-white hover:text-primary hover:shadow-lg hover:shadow-black/80"
						>jeepney phaseout</button
					>
					<button
						class="rounded-full bg-zinc-900 px-6 py-3 text-lg font-semibold text-white shadow-md shadow-black/50 duration-200 ease-in hover:scale-110 hover:bg-white hover:text-primary hover:shadow-lg hover:shadow-black/80"
						>modern</button
					>
					<button
						class="rounded-full bg-zinc-900 px-6 py-3 text-lg font-semibold text-white shadow-md shadow-black/50 duration-200 ease-in hover:scale-110 hover:bg-white hover:text-primary hover:shadow-lg hover:shadow-black/80"
						>modernisasyon</button
					>
					<button
						class="rounded-full bg-zinc-900 px-6 py-3 text-lg font-semibold text-white shadow-md shadow-black/50 duration-200 ease-in hover:scale-110 hover:bg-white hover:text-primary hover:shadow-lg hover:shadow-black/80"
						>modernization</button
					>
					<button
						class="rounded-full bg-zinc-900 px-6 py-3 text-lg font-semibold text-white shadow-md shadow-black/50 duration-200 ease-in hover:scale-110 hover:bg-white hover:text-primary hover:shadow-lg hover:shadow-black/80"
						>phaseout</button
					>
					<button
						class="rounded-full bg-zinc-900 px-6 py-3 text-lg font-semibold text-white shadow-md shadow-black/50 duration-200 ease-in hover:scale-110 hover:bg-white hover:text-primary hover:shadow-lg hover:shadow-black/80"
						>puv</button
					>
					<button
						class="rounded-full bg-zinc-900 px-6 py-3 text-lg font-semibold text-white shadow-md shadow-black/50 duration-200 ease-in hover:scale-110 hover:bg-white hover:text-primary hover:shadow-lg hover:shadow-black/80"
						>puv modernization</button
					>
					<button
						class="rounded-full bg-zinc-900 px-6 py-3 text-lg font-semibold text-white shadow-md shadow-black/50 duration-200 ease-in hover:scale-110 hover:bg-white hover:text-primary hover:shadow-lg hover:shadow-black/80"
						>puv phaseout</button
					>
					<button
						class="rounded-full bg-zinc-900 px-6 py-3 text-lg font-semibold text-white shadow-md shadow-black/50 duration-200 ease-in hover:scale-110 hover:bg-white hover:text-primary hover:shadow-lg hover:shadow-black/80"
						>strike</button
					>
				</div>
			</div>
		</div>
	</section>
	<section class="bg-gradient-radial-bottom from-primary/40 dark:from-primary/60 to-transparent" id="team">
		<div class="z-20 mx-auto flex max-w-6xl flex-col gap-6 px-4 py-20">
			<div class="z-10 flex flex-col items-center">
				<h1
					class="font-jeepney text-8xl font-extrabold tracking-tight text-pink-600 drop-shadow-md"
				>
					04
				</h1>
				<h1 class="font-jeep text-7xl uppercase tracking-tight text-orange-500 drop-shadow-md">
					Who are we?
				</h1>
			</div>
			<div class="grid auto-rows-auto grid-cols-6 gap-8">
				<div
					class="group col-span-2 row-span-1 items-center rounded-3xl border-2 border-secondary bg-background p-8 text-center drop-shadow-lg duration-100 ease-in hover:bg-primary hover:shadow-2xl"
				>
					<HoverCard.Root>
						<HoverCard.Trigger>
							<div class="mb-4 flex justify-center">
								<Avatar.Root>
									<Avatar.Image src={JGAvatar} alt="Justin Gonzales" />
									<Avatar.Fallback>JG</Avatar.Fallback>
								</Avatar.Root>
							</div>
							<h3 class="scroll-m-20 text-2xl font-semibold tracking-tight group-hover:text-white">
								Justin Andrei<br />Gonzales
							</h3></HoverCard.Trigger
						>
						<HoverCard.Content>
							<div class="flex flex-1 items-center justify-center space-x-2">
								<Button
									variant="outline"
									size="icon"
									href="mailto:jcgonzales12@up.edu.ph"
									target="_blank"
								>
									<i class="fa-solid fa-envelope fa-lg"></i>
								</Button>
							</div></HoverCard.Content
						>
					</HoverCard.Root>
					<p class="text-md leading-7 group-hover:text-white [&:not(:first-child)]:mt-6">
						I'm Justin, a 2nd year BS Computer Science student at the University of the Philippines,
						Diliman. With my interest in Computers and Technology, I am currently finding my passion
						where I can utilize my skills and help the community.
					</p>

					<p class="text-md leading-7 group-hover:text-white [&:not(:first-child)]:mt-6">
						In my free time, I enjoy watching K-dramas, playing video games like League of Legends
						and TFT. I also enjoy playing basketball whenever possible.
					</p>
				</div>
				<div
					class="group col-span-2 row-span-1 items-center rounded-3xl border-2 border-secondary bg-background p-8 text-center drop-shadow-lg duration-100 ease-in hover:bg-primary hover:shadow-2xl"
				>
					<HoverCard.Root>
						<HoverCard.Trigger>
							<div class="mb-4 flex justify-center">
								<Avatar.Root>
									<Avatar.Image src={GCAvatar} alt="Angelo Convento" />
									<Avatar.Fallback>GC</Avatar.Fallback>
								</Avatar.Root>
							</div>
							<h3 class="scroll-m-20 text-2xl font-semibold tracking-tight group-hover:text-white">
								Godfrey Angelo Convento
							</h3></HoverCard.Trigger
						>
						<HoverCard.Content>
							<div class="flex flex-1 items-center justify-center space-x-2">
								<Button
									variant="outline"
									size="icon"
									href="mailto:gaconvento@up.edu.ph"
									target="_blank"
								>
									<i class="fa-solid fa-envelope fa-lg"></i>
								</Button>
								<Button
									variant="outline"
									size="icon"
									href="https://github.com/conventoangelo"
									target="_blank"
								>
									<i class="fa-brands fa-github fa-lg"></i>
								</Button>
								<Button
									variant="outline"
									size="icon"
									href="https://www.linkedin.com/in/conventoangelo/"
									target="_blank"
								>
									<i class="fa-brands fa-linkedin fa-lg"></i>
								</Button>
							</div></HoverCard.Content
						>
					</HoverCard.Root>
					<p class="text-md leading-7 group-hover:text-white [&:not(:first-child)]:mt-6">
						Hey there! I'm Gelo, a 4th year BS Computer Science student at UP Diliman with a passion
						for front-end web development. I'm particularly interested in frameworks like Svelte and
						React. 
						</p><p class="text-md leading-7 group-hover:text-white [&:not(:first-child)]:mt-6">
						Lately, I've been diving into the world of productivity systems, exploring tools
						like Todoist and Notion Calendar to keep myself on top of things.
						</p> <p class="text-md leading-7 group-hover:text-white [&:not(:first-child)]:mt-6">When I need a break from the code, you might find me battling it
						out in DOTA 2 or Valorant. To unwind, I love jamming out to TWICE and BINI.
					</p>
				</div>
				<div
					class="group col-span-2 row-span-1 items-center rounded-3xl border-2 border-secondary bg-background p-8 text-center drop-shadow-lg duration-100 ease-in hover:bg-primary hover:shadow-2xl"
				>
					<HoverCard.Root>
						<HoverCard.Trigger>
							<div class="mb-4 flex justify-center">
								<Avatar.Root>
									<Avatar.Image src={ADAvatar} alt="Gelo De Leon" />
									<Avatar.Fallback>AD</Avatar.Fallback>
								</Avatar.Root>
							</div>
							<h3 class="scroll-m-20 text-2xl font-semibold tracking-tight group-hover:text-white">
								Angelo<br />De Leon
							</h3></HoverCard.Trigger
						>
						<HoverCard.Content>
							<div class="flex flex-1 items-center justify-center space-x-2">
								<Button
									variant="outline"
									size="icon"
									href="mailto:apdeleon4@up.edu.ph"
									target="_blank"
								>
									<i class="fa-solid fa-envelope fa-lg"></i>
								</Button>
							</div></HoverCard.Content
						>
					</HoverCard.Root>
					<p class="text-md leading-7 group-hover:text-white [&:not(:first-child)]:mt-6">
						Hi! I'm Gelo, a 2nd year Computer Science student from the University of the
						Philippines. Having the interest for both programming and graphic design, I became
						passionate in honing my creative and technical skills to make a meaningful difference in
						the world.
					</p>
					<p class="text-md leading-7 group-hover:text-white [&:not(:first-child)]:mt-6">
						Besides that, I mainly play games in my spare time. I enjoy games similar to Monster
						Hunter and Terraria, as well as some competitive games such as Valorant and TFT.
					</p>
				</div>
			</div>
		</div>
	</section>
</main>
