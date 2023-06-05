<script lang="ts">
	import Renderer from '../../components/Renderer/Renderer.svelte';
	import type { PaperComponent } from '$lib/types';
	const data: PaperComponent[] = [
		{
			id: 'Header',
			value: 'Hey I am a header'
		},
		{
			id: 'TextBox',
			value: 'This API helps you find your cat lost on the internet'
		}
	];
</script>

<div class=" m-auto w-[50%] border-x-4 border-black h-full p-2">
	<Renderer {data} />
</div>
