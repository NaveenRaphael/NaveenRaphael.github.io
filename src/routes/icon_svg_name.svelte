<script lang="ts">
	import { Icon, link_of_icon, text_of_icon } from '$lib/IconEnum.svelte';
	import IconSvg from './icon_svg.svelte';

	export let icon_type: Icon;
</script>

<div
	class="prose relative m-5 flex-none basis-1/5 rounded-xl border-4 border-transparent px-2 py-1 text-center text-2xl hover:prose-neutral dark:prose-invert hover:border-accent-600 lg:px-5"
>
	<IconSvg {icon_type} />
	<div class=" hidden translate-y-0.5 lg:inline-block">
		{text_of_icon(icon_type)}
	</div>
</div>
