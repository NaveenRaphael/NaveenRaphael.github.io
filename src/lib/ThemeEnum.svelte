<script lang="ts" module>
	import { writable } from 'svelte/store';

	enum Theme {
		Light,
		Dark
	}
	export let theme_toggle_letter = 'x';
	export function is_dark(theme: Theme): boolean {
		return theme == Theme.Dark;
	}
	export function to_str(theme: Theme): string {
		console.log('Changing theme...');
		if (is_dark(theme)) {
			return 'dark';
		}
		return ''; //Light theme does not need indication that it is light
	}

	function toggle(p: Theme): Theme {
		if (is_dark(p)) {
			return Theme.Light;
		} else {
			return Theme.Dark;
		}
	}

	function themeStore() {
		const { subscribe, set, update } = writable<Theme>(Theme.Dark);

		return {
			subscribe,
			toggle: () => update((theme) => toggle(theme)),
			reset: () => set(Theme.Dark)
		};
	}

	export const theme = themeStore();
</script>
