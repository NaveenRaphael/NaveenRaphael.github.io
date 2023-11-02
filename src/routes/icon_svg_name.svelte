<script lang="ts">
	import { Icon, link_of_icon, text_of_icon } from '$lib/IconEnum.svelte';
	import IconSvg from './icon_svg.svelte';

	export let icon_type: Icon;
	let t = text_of_icon(icon_type);
</script>

<div
	class="prose relative m-5 flex-none basis-1/5 rounded-full border-4 border-transparent px-2 pb-2 text-center text-2xl hover:prose-neutral dark:prose-invert hover:border-accent-600 lg:px-5"
>
	<IconSvg {icon_type} />
	{#if t != ''}
		<div class=" hidden translate-y-0.5 lg:inline-block">
			{text_of_icon(icon_type)}
		</div>
	{/if}
</div>
