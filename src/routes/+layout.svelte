<script lang="ts">
	import '../app.css';
	import { to_str, theme, theme_toggle_letter } from '$lib/ThemeEnum.svelte';

	$: dark = to_str($theme);

	function key_press(e: KeyboardEvent) {
		if (e.key == theme_toggle_letter) {
			theme.toggle();
		}
		console.log('Registered keyboard event!');
	}

	import MyNavBar from './myNavBar.svelte';
</script>

<div class="w-screen" class:dark>
	<div class="min-h-screen bg-gray-100 transition-all dark:bg-accent-950">
		<MyNavBar />
		<hr class="bg-accent-900 dark:bg-white" />
		<div class="prose min-w-full text-2xl dark:prose-invert">
			<slot />
		</div>
	</div>
</div>
<svelte:window on:keypress={key_press} />
