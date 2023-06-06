<script lang="ts">
	import Renderer from '../../components/Renderer/Renderer.svelte';
	import type { PaperComponent } from '$lib/types';
	import ComponentList from '../../components/ComponentsList/ComponentList.svelte';
	import PaperInfo from '../../components/PaperInfo/PaperInfo.svelte';
	let data: PaperComponent[] = [
	];
</script>

<div class=" overflow-y-scroll m-auto w-full h-full flex">
	<section class="w-[25%] h-full">
		<PaperInfo data={ { version:"1", visibility:"public", author:"Ze Waise Pizong" } }  />
	</section>
	<section class="w-[50%] border-x border-black h-full m-auto p-2">
		<Renderer {data} />
	</section>
	<section class="w-[25%] h-full">
		<ComponentList />
	</section>
</div>
