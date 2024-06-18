<script lang="ts">
	import { onMount } from 'svelte';
	import Autoplay from 'embla-carousel-autoplay';
	import * as Carousel from '$lib/components/ui/carousel/index.js';
	import * as Card from '$lib/components/ui/card';
	import * as HoverCard from '$lib/components/ui/hover-card/index.js';
	import * as Avatar from '$lib/components/ui/avatar/index.js';
	import * as Dialog from '$lib/components/ui/dialog/index.js';
	import { Button } from '$lib/components/ui/button/index.js';
	import { buttonVariants } from '$lib/components/ui/button';
	import Navigation from '$lib/Navigation.svelte';
	import ChevronsUpDown from 'lucide-svelte/icons/chevrons-up-down';
	import Database from 'lucide-svelte/icons/database';
	import jeep1 from '$lib/assets/jeep1.jpg';
	import RQ1 from '$lib/assets/RQ1.png';
	import RQ2 from '$lib/assets/RQ2.png';
	import GCAvatar from '$lib/assets/_DSC3637_512x512.png';
	import ADAvatar from '$lib/assets/435194078_981985919488202_6376095500813041272_n.png';
	import JGAvatar from '$lib/assets/435201424_342404608842278_1262981411790175769_n.jpg';
	import * as Collapsible from '$lib/components/ui/collapsible';
	import { Separator } from '$lib/components/ui/separator';
	let theme: string;
	// On component mount
	onMount(() => {
		// Check if the html element has the class 'dark'
		theme = document.documentElement.classList.contains('dark') ? 'dark' : 'light';
	});

	const plugin = Autoplay({ delay: 3000, stopOnInteraction: true });
</script>

<Navigation />
<main>
	<section
		class="w-full bg-gradient-radial-top from-blue-300/80 to-transparent dark:from-primary/10"
	>
		<div
			class="min-h-screen-minus-navbar mx-auto flex max-w-6xl flex-col items-center justify-center gap-2 py-16 pt-12 text-center"
		>
			<h1 class="leading-1.1 text-3xl font-bold tracking-tighter drop-shadow-xl sm:text-6xl">
				#Jeepney<span class="text-muted line-through decoration-destructive decoration-wavy"
					>Moder</span
				>N<span class="text-muted line-through decoration-destructive decoration-wavy">iz</span
				>ation
			</h1>
			<h1
				class="leading-1.1 text-2xl font-bold tracking-tighter text-primary drop-shadow-lg sm:text-5xl"
			>
				Sentiments on PUVMP
			</h1>
			<p class="max-w-[350px ]text-sm mb-6 text-muted-foreground sm:max-w-[750px] sm:text-lg">
				A Twitter analysis of Filipino reception towards Jeepney Modernization
			</p>
			<Carousel.Root
				class="w-full max-w-xs sm:max-w-2xl"
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
				<Carousel.Previous class="hidden md:flex" />
				<Carousel.Next class="hidden md:flex" />
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
			class="z-20 mx-16 max-w-[850px] text-2xl font-medium leading-tight hover:drop-shadow-2xl md:text-3xl [&:not(:first-child)]:mt-6"
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
		class="mx-auto flex h-full max-w-6xl grid-cols-2 flex-col items-center gap-8 px-4 py-20 md:grid md:h-screen md:gap-16"
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
			<div class="flex auto-rows-auto grid-cols-4 flex-col gap-8 md:grid">
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
									<a
										href="https://ltfrb.gov.ph/puv-modernization-program/"
										target="_blank"
										rel="noreferrer noopener"
									>
										<img
											src="https://ltfrb.gov.ph/wp-content/uploads/2023/05/PUVMP-logo-1536x1027.png"
											alt="PUVMP Banner"
											class="rounded-md"
										/>
										<p class="text-md mt-2 font-semibold">LTFRB | PUV Modernization Program</p>
									</a>
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
									<a
										href="https://changing-transport.org/modernizing-public-transport-in-the-philippines/"
										target="_blank"
										rel="noreferrer noopener"
									>
										<img
											src="https://changing-transport.org/wp-content/uploads/MicrosoftTeams-image-1024x768.jpg"
											alt="Modern Electric Jeepney"
											class="rounded-md"
										/>
										<p class="text-md mt-2 font-semibold">
											Changing Transport | Modernizing Public Transport in the Philippines
										</p>
									</a>
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
									<a
										href="https://www.rappler.com/business/summary-recap-transport-strike-spotlights-jeepney-modernization-issues-march-6-2023/"
										target="_blank"
										rel="noreferrer noopener"
									>
										<img
											src="https://www.rappler.com/tachyon/2023/03/jeepney-stike-puv-modernization-drivers-protest-march-6-2023-001-scaled.jpg?resize=2560%2C1707&zoom=1"
											alt="Jeepney driver with #NoToPUVPhaseout placard"
											class="rounded-md"
										/>
										<p class="text-md mt-2 font-semibold">
											Rappler (Lance Yu) | ‘Welga kami!’ Transport strike spotlights jeepney
											modernization issues
										</p>
									</a>
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
					<h2 class="scroll-m-20 pb-2 text-3xl font-bold tracking-tight">Research Questions</h2>
					<ol>
						<li class="text-lg leading-7 [&:not(:first-child)]:mt-6">
							1. What is the general reaction of the population regarding the PUV Modernization
							Program?
						</li>
						<li class="text-lg leading-7 [&:not(:first-child)]:mt-6">
							2. What are the frequent words used when the user activity increases?
						</li>
					</ol>
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
						The ratio of positive to negative tweets is constant throughout the study period.
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
						The ratio of positive to negative tweets significantly changes throughout the study
						period.
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
			<h1
				class="text-right font-jeep text-7xl uppercase tracking-tight text-green-500 drop-shadow-lg"
			>
				Materials and Methods
			</h1>
			<div class="flex flex-col items-end gap-4 sm:flex-row">
				<a
					href="https://docs.google.com/spreadsheets/d/12IpBDpizXs0iUv-_JWSdayhhISXB46U-ikx9F7g1sbY/edit#gid=0"
					target="_blank"
					rel="noreferrer noopener"
					class={buttonVariants({ variant: 'outline' })}
				>
					<Database class="mr-2 h-4 w-4" />
					<p class="justify-end">Explore the dataset here</p></a
				>
				<a
					href="https://colab.research.google.com/drive/1_0Ua2sbmbo0mzbNshLNY-L0tHrWosjAW?authuser=1#scrollTo=H2QHb34dorUC"
					target="_blank"
					rel="noreferrer noopener"
					class={buttonVariants({ variant: 'outline' })}
					><i class="fa-solid fa-up-right-from-square mr-2"></i>
					<p class="">View our data exploration here</p></a
				>
			</div>
		</div>
		<div class="flex auto-rows-auto grid-cols-6 flex-col gap-8 md:grid">
			<div
				class="group col-span-6 flex flex-col items-center gap-4 rounded-3xl bg-secondary bg-cover bg-bottom p-8 drop-shadow-lg duration-100 ease-in hover:bg-jeep3 hover:shadow-2xl"
			>
				<h2 class="scroll-m-20 pb-3 text-4xl font-bold tracking-tight group-hover:text-white">
					Keywords
				</h2>
				<div class="flex max-w-4xl flex-wrap items-center justify-center gap-x-4 gap-y-3">
					<button
						class="rounded-full bg-zinc-900 px-6 py-3 text-sm font-semibold text-white shadow-md shadow-black/50 duration-200 ease-in hover:scale-110 hover:bg-white hover:text-primary hover:shadow-lg hover:shadow-black/80 sm:text-lg"
						>electric</button
					>
					<button
						class="rounded-full bg-zinc-900 px-6 py-3 text-sm font-semibold text-white shadow-md shadow-black/50 duration-200 ease-in hover:scale-110 hover:bg-white hover:text-primary hover:shadow-lg hover:shadow-black/80 sm:text-lg"
						>jeep</button
					>
					<button
						class="rounded-full bg-zinc-900 px-6 py-3 text-sm font-semibold text-white shadow-md shadow-black/50 duration-200 ease-in hover:scale-110 hover:bg-white hover:text-primary hover:shadow-lg hover:shadow-black/80 sm:text-lg"
						>jeepney</button
					>
					<button
						class="rounded-full bg-zinc-900 px-6 py-3 text-sm font-semibold text-white shadow-md shadow-black/50 duration-200 ease-in hover:scale-110 hover:bg-white hover:text-primary hover:shadow-lg hover:shadow-black/80 sm:text-lg"
						>jeepney modernization</button
					>
					<button
						class="rounded-full bg-zinc-900 px-6 py-3 text-sm font-semibold text-white shadow-md shadow-black/50 duration-200 ease-in hover:scale-110 hover:bg-white hover:text-primary hover:shadow-lg hover:shadow-black/80 sm:text-lg"
						>jeepney phaseout</button
					>
					<button
						class="rounded-full bg-zinc-900 px-6 py-3 text-sm font-semibold text-white shadow-md shadow-black/50 duration-200 ease-in hover:scale-110 hover:bg-white hover:text-primary hover:shadow-lg hover:shadow-black/80 sm:text-lg"
						>modern</button
					>
					<button
						class="rounded-full bg-zinc-900 px-6 py-3 text-sm font-semibold text-white shadow-md shadow-black/50 duration-200 ease-in hover:scale-110 hover:bg-white hover:text-primary hover:shadow-lg hover:shadow-black/80 sm:text-lg"
						>modernisasyon</button
					>
					<button
						class="rounded-full bg-zinc-900 px-6 py-3 text-sm font-semibold text-white shadow-md shadow-black/50 duration-200 ease-in hover:scale-110 hover:bg-white hover:text-primary hover:shadow-lg hover:shadow-black/80 sm:text-lg"
						>modernization</button
					>
					<button
						class="rounded-full bg-zinc-900 px-6 py-3 text-sm font-semibold text-white shadow-md shadow-black/50 duration-200 ease-in hover:scale-110 hover:bg-white hover:text-primary hover:shadow-lg hover:shadow-black/80 sm:text-lg"
						>phaseout</button
					>
					<button
						class="rounded-full bg-zinc-900 px-6 py-3 text-sm font-semibold text-white shadow-md shadow-black/50 duration-200 ease-in hover:scale-110 hover:bg-white hover:text-primary hover:shadow-lg hover:shadow-black/80 sm:text-lg"
						>puv</button
					>
					<button
						class="rounded-full bg-zinc-900 px-6 py-3 text-sm font-semibold text-white shadow-md shadow-black/50 duration-200 ease-in hover:scale-110 hover:bg-white hover:text-primary hover:shadow-lg hover:shadow-black/80 sm:text-lg"
						>puv modernization</button
					>
					<button
						class="rounded-full bg-zinc-900 px-6 py-3 text-sm font-semibold text-white shadow-md shadow-black/50 duration-200 ease-in hover:scale-110 hover:bg-white hover:text-primary hover:shadow-lg hover:shadow-black/80 sm:text-lg"
						>puv phaseout</button
					>
					<button
						class="rounded-full bg-zinc-900 px-6 py-3 text-sm font-semibold text-white shadow-md shadow-black/50 duration-200 ease-in hover:scale-110 hover:bg-white hover:text-primary hover:shadow-lg hover:shadow-black/80 sm:text-lg"
						>strike</button
					>
				</div>
			</div>
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
		</div>
		<Collapsible.Root class="mt-4 w-full space-y-4">
			<Collapsible.Trigger asChild let:builder>
				<div class="flex items-center justify-between space-x-4 px-4">
					<Button builders={[builder]} variant="link" class="p-0 text-foreground">
						<div class="flex-col">
							<h4 class="hidden text-2xl font-semibold sm:flex">Natural Language Processing</h4>
							<h4 class="flex text-left text-2xl font-semibold sm:hidden">
								Natural Language<br />Processing
							</h4>
						</div>
					</Button>
					<Button builders={[builder]} variant="ghost" size="sm" class="w-9 p-0">
						<ChevronsUpDown class="h-4 w-4" />
						<span class="sr-only">Toggle</span>
					</Button>
				</div>
			</Collapsible.Trigger>
			<Collapsible.Content class="space-y-2">
				<div class="px-4 py-3">
					<p class="text-lg leading-7 [&:not(:first-child)]:mt-6">
						The tweets were processed using Natural Language Processing (NLP) techniques. However,
						due to the Filipino language content, additional steps were required:
					</p>
					<ol class="mt-2 list-decimal pl-10">
						<li class="text-lg leading-7">
							<span class="font-bold">Translation:</span> The Filipino content was translated into English
							using GoogleTrans. This was necessary to ensure the accuracy of the subsequent NLP steps.
						</li>
						<li class="text-lg leading-7">
							<span class="font-bold">Manual Checking:</span> The translated content was manually checked
							to ensure the accuracy of the translation. This was important to maintain the context and
							meaning of the original content.
						</li>
					</ol>
					<h5
						class="text-xl font-bold leading-7 decoration-2 hover:underline [&:not(:first-child)]:mt-6"
					>
						Cleaning the Filipino Tweets
					</h5>
					<p class="text-lg leading-7 [&:not(:first-child)]:mt-3">
						The Filipino content required additional cleaning to improve the accuracy of the
						translation. This involved:
					</p>
					<ol class="mt-2 list-decimal pl-10">
						<li class="text-lg leading-7">
							<span class="font-bold">Changing Filipino Slang:</span> Filipino slang and shorthand were
							converted into formal words to improve the accuracy of the translation.
						</li>
						<li class="text-lg leading-7">
							<span class="font-bold">Tokenization:</span> Tweets are broken down into words or phrases
							according to what's more appropriate for the analysis.
						</li>
					</ol>
					<h5
						class="text-xl font-bold leading-7 decoration-2 hover:underline [&:not(:first-child)]:mt-6"
					>
						Translating the Tweets
					</h5>
					<p class="text-lg leading-7 [&:not(:first-child)]:mt-3">
						GoogleTrans was used to translate the cleaned Filipino content into English. The
						translated content was then further cleaned by:
					</p>
					<ol class="mt-2 list-decimal pl-10">
						<li class="text-lg leading-7">
							<span class="font-bold">Lowercasing:</span> All the translated content was converted to
							lowercase to maintain consistency.
						</li>
						<li class="text-lg leading-7">
							<span class="font-bold">Removing Punctuation Marks:</span> All punctuation marks were removed
							from the translated content to simplify the subsequent NLP steps.
						</li>
					</ol>
					<h5
						class="text-xl font-bold leading-7 decoration-2 hover:underline [&:not(:first-child)]:mt-6"
					>
						Manual Correction of the Translation
					</h5>
					<p class="text-lg leading-7 [&:not(:first-child)]:mt-3">
						The translated tweets was manually checked and corrected to improve the context
						accuracy, fix erroneous spacing, and catch mistakes. The manually corrected tweets was
						then used in the subsequent analysis.
					</p>
				</div>
			</Collapsible.Content>
		</Collapsible.Root>
		<Separator />
		<Collapsible.Root class="w-full space-y-4">
			<Collapsible.Trigger asChild let:builder>
				<div class="flex items-center justify-between space-x-4 px-4">
					<Button builders={[builder]} variant="link" class="p-0 text-foreground">
						<h4 class="text-2xl font-semibold">Visualization</h4>
					</Button>
					<Button builders={[builder]} variant="ghost" size="sm" class="w-9 p-0">
						<ChevronsUpDown class="h-4 w-4" />
						<span class="sr-only">Toggle</span>
					</Button>
				</div>
			</Collapsible.Trigger>
			<Collapsible.Content class="space-y-2">
				<div class="px-4 py-3">
					<p class="text-lg leading-7 [&:not(:first-child)]:mt-6">
						Effective communication of research findings extends beyond mere textual presentation.
						Recognizing this, we leveraged the power of data visualization to transform our insights
						into readily comprehensible graphs and charts. This visual approach fosters a clear
						understanding of the data for a broader audience.
					</p>
					<h5
						class="text-xl font-bold leading-7 decoration-2 hover:underline [&:not(:first-child)]:mt-6"
					>
						Frequency of Tweets about Jeepney Modernization
					</h5>
					<p class="text-lg leading-7 [&:not(:first-child)]:mt-3">
						The frequency of tweets about jeepney modernization in the Philippines saw a distinct
						peak in <span class="font-semibold">March 2023</span>. This initial surge subsided, but
						the conversation reignited in
						<span class="font-semibold">December 2023</span> as the deadline for jeepney
						modernization loomed on December 31st. The subsequent extension of the deadline to
						<span class="font-semibold">April 2024</span> triggered another rise in tweet frequency.
					</p>
					<Dialog.Root>
						<Dialog.Trigger
							><img
								src={RQ1}
								alt="Monthly Number of Tweets"
								class="mt-4 w-full rounded-lg object-cover"
							/></Dialog.Trigger
						>
						<Dialog.Content class="max-w-screen">
							<div class="flex flex-col gap-4 py-4 md:grid">
								<img
									src={RQ1}
									alt="Monthly Number of Tweets"
									class="mt-4 w-full rounded-lg object-cover"
								/>
							</div>
						</Dialog.Content>
					</Dialog.Root>
					<h5
						class="text-xl font-bold leading-7 decoration-2 hover:underline [&:not(:first-child)]:mt-6"
					>
						NLP Word Frequency Visualization
					</h5>
					<p class="text-lg leading-7 [&:not(:first-child)]:mt-3">
						Building on the previous graph that highlighted peak tweet volume in March 2023,
						December 2023, and April 2024, this NLP Word Frequency Visualization delves deeper into
						the sentiment expressed during those periods. Notably, March 2023 appears to have a
						higher concentration of positive terms compared to the other months. However, negative
						sentiment regarding jeepney modernization is also evident, with terms like "no to
						jeepney phaseout" standing out.
					</p>
					<Dialog.Root>
						<Dialog.Trigger>
							<img
								src={RQ2}
								alt="Most Frequently Used Words"
								class="mt-4 w-full rounded-lg object-cover"
							/></Dialog.Trigger
						>
						<Dialog.Content class="max-w-screen">
							<div class="flex flex-col gap-4 py-4 md:grid">
								<img
									src={RQ2}
									alt="Most Frequently Used Words"
									class="mt-4 w-full rounded-lg object-cover"
								/>
							</div>
						</Dialog.Content>
					</Dialog.Root>
				</div>
			</Collapsible.Content>
		</Collapsible.Root>
		<Separator />
		<Collapsible.Root class="w-full space-y-4">
			<Collapsible.Trigger asChild let:builder>
				<div class="flex items-center justify-between space-x-4 px-4">
					<Button builders={[builder]} variant="link" class="p-0 text-foreground">
						<h4 class="text-2xl font-semibold">Testing</h4>
					</Button>
					<Button builders={[builder]} variant="ghost" size="sm" class="w-9 p-0">
						<ChevronsUpDown class="h-4 w-4" />
						<span class="sr-only">Toggle</span>
					</Button>
				</div>
			</Collapsible.Trigger>
			<Collapsible.Content class="space-y-2">
				<div class="px-4 py-3">
					<p class="text-lg leading-7 [&:not(:first-child)]:mt-6">
						Following data visualization, we employed the Chi Squared Test of Independence to test
						if the tweet sentiment is affected by time.
					</p>

					<ul class="my-6 ml-6 list-disc text-lg [&>li]:mt-2">
						<li>
							Null hypothesis (H<sub>0</sub>): The ratio of positive to negative tweets is constant
							throughout the study period. (Tweet sentiment is independent of time)
						</li>
						<li>
							Alternative hypothesis (H<sub>a</sub>): The ratio of positive to negative tweets
							significantly changes throughout the study period. (Tweet sentiment is dependent on
							time)
						</li>
					</ul>
					<p class="text-lg leading-7 [&:not(:first-child)]:mt-6">
						We formed groups of 5 for the number of tweets per sentiment per month to meet the
						requirement of the statement: (<code
							class="text-md relative rounded bg-muted px-[0.3rem] py-[0.2rem] font-mono font-semibold text-green-700 dark:text-green-300"
							>observed >= 5</code
						>)
					</p>
					<ul class="my-6 ml-6 list-disc text-lg [&>li]:mt-2">
						<li>
							Chi-Square Statistic: <span
								class="text-md relative rounded bg-muted px-[0.3rem] py-[0.2rem] font-mono font-semibold"
								>14.120520497226948</span
							>
						</li>
						<li>
							P-value: <span
								class="text-md relative rounded bg-muted px-[0.3rem] py-[0.2rem] font-mono font-semibold"
								>0.014861708645671878
							</span>
						</li>
						<li>
							Degrees of Freedom: <span
								class="text-md relative rounded bg-muted px-[0.3rem] py-[0.2rem] font-mono font-semibold"
								>5
							</span>
						</li>
						<li>
							Expected Frequency: <span
								class="text-md relative rounded bg-muted px-[0.3rem] py-[0.2rem] font-mono font-semibold"
								>[[ 24.82399103 96.17600897] [ 10.25784753 39.74215247] [ 44.10874439 170.89125561]
								[ 13.95067265 54.04932735] [ 55.80269058 216.19730942] [ 34.05605381 131.94394619]]
							</span>
						</li>
						<li>
							Decision: <span
								class="text-md relative rounded bg-muted px-[0.3rem] py-[0.2rem] font-mono font-semibold"
								>p&lt;=0.05, <span class="font-bold text-red-500"> Reject Null Hypothesis </span>
							</span>
						</li>
					</ul>
				</div>
			</Collapsible.Content>
		</Collapsible.Root>
		<Separator />
	</section>

	<section
		class="w-full bg-gradient-radial-top from-blue-300/80 to-transparent dark:from-primary/10"
		id="machinelearning"
	>
		<div class="mx-auto flex max-w-4xl flex-col items-center gap-6 px-4 py-20 text-center">
			<div>
				<h1
					class="font-jeepney text-8xl font-extrabold tracking-tight text-orange-400 drop-shadow-md dark:text-orange-400"
				>
					04
				</h1>
				<h1 class="font-jeep text-7xl uppercase tracking-tight text-violet-500 drop-shadow-lg">
					Machine Learning
				</h1>
				<Button variant="outline"
				><a class="flex items-center justify-center space-x-2"
					target="_blank"
					href="https://colab.research.google.com/drive/1iF-sZdCyK_fl5Yoye69RGQGlZGINgaLe#scrollTo=E2Kr_i1uxfkW&line=3&uniqifier=1"
					><i class="fa-solid fa-up-right-from-square"></i>
					<p class="">View the LDA model here</p></a
				></Button
			>
			</div>
			<div
				class="rounded-3xl bg-secondary p-8 drop-shadow-lg duration-100 ease-in hover:bg-primary hover:text-white hover:shadow-2xl"
			>
				<h2 class="scroll-m-20 text-2xl font-semibold tracking-tight">
					Extracting Topic Modeling Features using LDA (Latent Dirichlet Allocation)
				</h2>
				<p class="text-md leading-7 [&:not(:first-child)]:mt-6">
					In natural language processing, Latent Dirichlet Allocation (LDA) is a generative
					statistical model (unsupervised) that explains a set of observations through unobserved
					groups, and each group explains why some parts of the data are similar. The LDA is an
					example of a topic model. In this, observations (i.e., words) are collected into
					documents, and each word's presence is attributable to one of the document's topics. Each
					document will contain a small number of topics.
				</p>
			</div>
		</div>
	</section>

	<section
		class="bg-gradient-radial-bottom from-primary/40 to-transparent dark:from-primary/60"
		id="team"
	>
		<div class="z-20 mx-auto flex max-w-6xl flex-col gap-6 px-4 py-20">
			<div class="z-10 flex flex-col items-center">
				<h1
					class="font-jeepney text-8xl font-extrabold tracking-tight text-pink-600 drop-shadow-md"
				>
					05
				</h1>
				<h1 class="font-jeep text-7xl uppercase tracking-tight text-orange-500 drop-shadow-md">
					Who are we?
				</h1>
			</div>
			<div class="flex auto-rows-auto grid-cols-6 flex-col gap-8 md:grid">
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
					<div class="mt-2 flex flex-1 items-center justify-center space-x-2 md:hidden">
						<Button
							variant="outline"
							size="icon"
							href="mailto:jcgonzales12@up.edu.ph"
							target="_blank"
						>
							<i class="fa-solid fa-envelope fa-lg"></i>
						</Button>
					</div>
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
					<div class="mt-2 flex flex-1 items-center justify-center space-x-2 md:hidden">
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
					</div>
					<p class="text-md leading-7 group-hover:text-white [&:not(:first-child)]:mt-6">
						Hey there! I'm Gelo, a 4th year BS Computer Science student at UP Diliman with a passion
						for front-end web development. I'm particularly interested in frameworks like Svelte and
						React.
					</p>
					<p class="text-md leading-7 group-hover:text-white [&:not(:first-child)]:mt-6">
						Lately, I've been diving into the world of productivity systems, exploring tools like
						Todoist and Notion Calendar to keep myself on top of things.
					</p>
					<p class="text-md leading-7 group-hover:text-white [&:not(:first-child)]:mt-6">
						When I need a break from the code, you might find me battling it out in DOTA 2 or
						Valorant. To unwind, I love jamming out to TWICE and BINI.
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
					<div class="mt-2 flex flex-1 items-center justify-center space-x-2 md:hidden">
						<Button variant="outline" size="icon" href="mailto:apdeleon4@up.edu.ph" target="_blank">
							<i class="fa-solid fa-envelope fa-lg"></i>
						</Button>
					</div>
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
