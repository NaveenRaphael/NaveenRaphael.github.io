<script lang="ts" context="module">
	export enum Theme {
		Light,
		Dark
	}

	export function is_dark(theme: Theme): boolean {
		return theme == Theme.Dark;
	}
	export function to_str(theme: Theme): string {
		if (is_dark(theme)) {
			return 'dark';
		}
		return 'light';
	}
</script>
