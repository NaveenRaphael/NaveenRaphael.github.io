<script lang="ts">
	import { createEventDispatcher } from 'svelte';
	import { Theme } from '$lib/ThemeEnum.svelte';
	import { is_dark } from '$lib/ThemeEnum.svelte';

	let present_theme = Theme.Light;

	const dispatch = createEventDispatcher<{ theme: Theme }>();

	function toggle() {
		if (is_dark(present_theme)) {
			present_theme = Theme.Light;
		} else {
			present_theme = Theme.Dark;
		}
		dispatch('theme', present_theme);
	}
</script>

<div class="absolute bottom-2 right-2">
	<button on:click={toggle}>
		<svg
			xmlns="http://www.w3.org/2000/svg"
			fill="none"
			viewBox="0 0 24 24"
			stroke-width="1.6"
			class="h-8 w-8 rounded-lg bg-slate-400 stroke-current dark:bg-slate-800 dark:stroke-slate-100"
		>
			{#if is_dark(present_theme)}
				<path
					stroke-linecap="round"
					stroke-linejoin="round"
					d="M12 3v2.25m6.364.386l-1.591 1.591M21 12h-2.25m-.386 6.364l-1.591-1.591M12 18.75V21m-4.773-4.227l-1.591 1.591M5.25 12H3m4.227-4.773L5.636 5.636M15.75 12a3.75 3.75 0 11-7.5 0 3.75 3.75 0 017.5 0z"
				/>
			{:else}
				<path
					stroke-linecap="round"
					stroke-linejoin="round"
					d="M21.752 15.002A9.718 9.718 0 0118 15.75c-5.385 0-9.75-4.365-9.75-9.75 0-1.33.266-2.597.748-3.752A9.753 9.753 0 003 11.25C3 16.635 7.365 21 12.75 21a9.753 9.753 0 009.002-5.998z"
				/>
			{/if}
		</svg>
	</button>
</div>
