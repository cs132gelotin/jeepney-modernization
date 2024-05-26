<script lang="ts">
	import Sun from 'lucide-svelte/icons/sun';
	import Moon from 'lucide-svelte/icons/moon';
	import { toggleMode } from 'mode-watcher';
	import { Button } from '$lib/components/ui/button/index.js';
	import { base } from '$app/paths';
	import  logo from '$lib/assets/logo.png';
</script>

<header
	class="sticky top-0 z-50 w-full border-b border-border/40 bg-background/95 backdrop-blur supports-[backdrop-filter]:bg-background/60"
>
	<div class="container flex h-14 max-w-screen items-center">
		<div class="bg-slate mr-4 flex flex-row">
			<a href={base} class="mr-6 flex items-center">
				<img
					src={logo}
					alt="JeepneyNation"
					class="h-8 w-auto">
				<!-- <p class="font-bold text-primary">JeepneyNation</p> -->
			</a>
			<nav class="sm:flex items-center text-center gap-6 text-sm hidden">
				<a
					href={`${base}#overview`}
					class="text-foreground/60 transition-colors hover:text-foreground/80">Overview</a
				>
				<a
					href={`${base}#problem`}
					class="text-foreground/60 transition-colors hover:text-foreground/80">Problem</a
				>
				<a
					href={`${base}#materials&methods`}
					class="text-foreground/60 transition-colors hover:text-foreground/80"
					>Materials and Methods</a
				>
				<a
					href={`${base}#team`}
					class="text-foreground/60 transition-colors hover:text-foreground/80">Team</a
				>
			</nav>
		</div>
		<nav class="flex flex-1 items-center space-x-2 justify-end">
			<Button
				variant="outline"
				size="icon"
				href="https://github.com/cs132gelotin/jeepney-modernization"
				target="_blank"
			>
				<i class="fa-brands fa-github fa-lg"></i>
			</Button>
			<Button on:click={toggleMode} variant="outline" size="icon">
				<Sun
					class="h-[1.2rem] w-[1.2rem] rotate-0 scale-100 transition-all dark:-rotate-90 dark:scale-0"
				/>
				<Moon
					class="absolute h-[1.2rem] w-[1.2rem] rotate-90 scale-0 transition-all dark:rotate-0 dark:scale-100"
				/>
				<span class="sr-only">Toggle theme</span>
			</Button>
		</nav>
	</div>
</header>
