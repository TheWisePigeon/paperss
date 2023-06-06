<script lang="ts">
	import Renderer from '../../components/Renderer/Renderer.svelte';
	import type { PaperComponent } from '$lib/types';
    import ComponentList from '../../components/ComponentsList/ComponentList.svelte';
    import PaperInfo from '../../components/PaperInfo/PaperInfo.svelte';
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

<div class=" overflow-y-scroll m-auto w-full h-full flex ">
    <section class="w-[25%] h-full" >
        <PaperInfo />
    </section>
    <section class="w-[50%] border-x-2 border-black h-full m-auto p-2" >
        <Renderer {data} />
    </section>
    <section class="w-[25%] h-full" >
        <ComponentList />
    </section>
</div>
