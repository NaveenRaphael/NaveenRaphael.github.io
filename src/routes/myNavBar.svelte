<script>
	import IconAndName from './icon_svg_name.svelte';
	import IconEnum, { Icon, link_of_icon } from '$lib/IconEnum.svelte';
	import { is_dark, theme } from '$lib/ThemeEnum.svelte';
	let types = [Icon.Home, Icon.Study, Icon.Contact];
</script>

<nav class="flex flex-wrap place-content-around">
	<!-- Links -->
	{#each types as t}
		<a href={link_of_icon(t)}>
			<IconAndName icon_type={t} />
		</a>
	{/each}

	<!-- Theme toggle -->
	<button onclick={theme.toggle}>
		<IconAndName icon_type={is_dark($theme) ? Icon.Dark_Theme : Icon.Light_Theme} />
	</button>
</nav>
