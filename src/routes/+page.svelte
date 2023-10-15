<script lang="ts">
	import '../app.css';
	import { Theme } from '$lib/ThemeEnum.svelte';
	import { is_dark, to_str } from '$lib/ThemeEnum.svelte';
	import MyRoutes from './MyRoutes.svelte';
	import ThemeToggle from './ThemeToggle.svelte';

	let present_theme = Theme.Dark;
	let theme = 'dark';
	const toggle_letter = 'x';

	function key_press(e: KeyboardEvent) {
		if (e.key == toggle_letter) {
			toggle();
		}
		console.log('Sigh');
	}
	function toggle() {
		if (is_dark(present_theme)) {
			present_theme = Theme.Light;
		} else {
			present_theme = Theme.Dark;
		}
		theme = to_str(present_theme);
	}

	function test(event: CustomEvent<Theme>) {
		if (event.detail == Theme.Light) {
			theme = 'light';
		} else {
			theme = 'dark';
		}
	}

	function has_keyboard() {
		//TODO: change the interaction menu completely
		return true;
	}
</script>

<!-- svelte-ignore a11y-no-static-element-interactions -->
<div class={theme + ' h-screen w-screen'}>
	<div class=" h-full w-full bg-gray-100 transition-all dark:bg-accent-950">
		<div class="float-right w-1/2 lg:w-1/4">
			<img src="mepic.png" alt="me" class="" />
		</div>
		<div
			title="Introduction"
			class="prose p-9 text-2xl dark:prose-invert lg:min-w-fit lg:p-20 lg:text-center"
		>
			<h1 class="text-5xl lg:text-7xl">Hello there!</h1>
			<p>This is the personal site of Naveen Raphael!</p>
			<p>
				Interested in machine learning and optimisation, I am presently working on pose estimation
				as a PMRF scholar in IIT Madras.
			</p>
			<p>Feel free to look around!</p>
		</div>

		<div
			class=" flex flex-wrap place-content-around justify-evenly justify-items-stretch gap-1 gap-3 object-center p-10"
		>
			<MyRoutes />
			<MyRoutes />
			<MyRoutes />
		</div>
		{#if has_keyboard()}
			<code class="prose prose-neutral absolute bottom-5 right-5 dark:prose-invert">
				Press [{toggle_letter}] to change theme!
			</code>
		{:else}
			<code class="prose prose-neutral absolute bottom-5 right-5 dark:prose-invert">
				Double tap to change theme!
			</code>
		{/if}
	</div>
	<!-- <ThemeToggle /> -->
</div>

<svelte:window on:keypress={key_press} on:dblclick={toggle} />
