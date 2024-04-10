<script lang="ts">
	import { onMount } from 'svelte';
	import Autoplay from 'embla-carousel-autoplay';
	import * as Carousel from '$lib/components/ui/carousel/index.js';
	import * as Card from '$lib/components/ui/card';

	let theme: string;
	// On component mount
	onMount(() => {
		// Check if the html element has the class 'dark'
		theme = document.documentElement.classList.contains('dark') ? 'dark' : 'light';
	});

	const plugin = Autoplay({ delay: 3000, stopOnInteraction: true });
</script>

<main>
	<div class="flex-1">
		<section
			class="mx-auto flex max-w-7xl flex-col items-center justify-center gap-2 pt-24 text-center"
		>
			<h1 class="leading-1.1 text-6xl font-bold tracking-tighter">#JeepneyNation</h1>
			<h1 class="leading-1.1 text-5xl font-bold tracking-tighter text-primary">
				Sentiments on Modernization
			</h1>
			<p class="mt-6 max-w-[750px] text-lg text-muted-foreground">
				A Twitter analysis of Filipino reception towards Jeepney Modernization
			</p>
			<Carousel.Root
				class="w-full max-w-2xl"
				plugins={[plugin]}
				on:mousenter={plugin.stop}
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
												Sara, Arjo, etc. don’t get it: among all people, it’s the jeepney drivers
												who will suffer the most, because no income for 7 days. But the move is
												drastic because their calls remain unheeded and their concerns, unaddressed.
												Grabe yung kakulangan ng pang unawa sa gubyernong ito.
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

		<section class="mx-auto grid max-w-7xl grid-cols-2 items-center gap-16 px-4 py-24 pb-20">
			<div>
				<h1 class="text-4xl font-extrabold tracking-tight">Overview</h1>
				<p class="mt-6">
					Lorem ipsum dolor sit amet consectetur adipisicing elit. Nostrum, distinctio suscipit sunt
					impedit voluptatibus quibusdam aliquam quod, totam dolorum delectus, excepturi ratione.
					Quidem dolorem porro exercitationem asperiores facere et quaerat?
				</p>
			</div>
			<div class="relative h-full">
				<img
					class="h-full w-full rounded-lg object-cover"
					src="https://scontent-sin6-2.xx.fbcdn.net/v/t39.30808-6/415484402_756029469879017_7177651367276687478_n.jpg?_nc_cat=108&ccb=1-7&_nc_sid=5f2048&_nc_eui2=AeH4NHdT9NHSFdHNchYqL8npH10ikwPlVFsfXSKTA-VUW1d6OEdJaXzLB0lkIu73bGTmOP2byDGfm-q3Li35TUL-&_nc_ohc=_3t4bnFE-q4Ab4N58rd&_nc_ht=scontent-sin6-2.xx&oh=00_AfBsEVb9H4zY81LnLUoH_pPupMZ8ol4MtH0LPQIa5ggYgg&oe=661C1167"
					alt="no to puv phaseout rally"
				/>
			</div>
		</section>
	</div>
</main>
