<script lang="ts">
	type PaperInfo = {
		version: string;
		author: string;
		visibility: 'public' | 'private';
	};
	export let data: PaperInfo;
</script>

<div class=" flex flex-col w-full h-full bg-red-400 p-2">
	<h1>Paper version : {data.version}</h1>
	<h1>Author : {data.author}</h1>
	<h1>Visibility : {data.visibility}</h1>
</div>
