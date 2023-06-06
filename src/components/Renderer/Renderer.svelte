<script lang="ts">
	import Header from '../Header/Header.svelte';
    import Paragraph from '../Paragraph/Paragraph.svelte';
	import type { SvelteComponent } from 'svelte';
	export let data: { id: string; value: string }[];
	const componentMap: Record<string, typeof SvelteComponent> = {
		Header,
		Paragraph
	};
	function render_component() {
		return data.map((component) => {
			const Component = componentMap[component.id];
			return {
				Component,
				props: {
					content: component.value
				}
			};
		});
	}
</script>

{#if data.length==0}
    <h1 class="text-center text-gray-500">Chose components from the right menu and start writing your paper</h1>
{/if}
{#each render_component() as { Component, props }}
	<svelte:component this={Component} content={props.content} />
{/each}
