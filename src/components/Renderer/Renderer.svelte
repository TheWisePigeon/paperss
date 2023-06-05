<script lang="ts">
	import Header from '../Header/Header.svelte';
	import TextBox from '../TextBox/TextBox.svelte';
	import type { SvelteComponent } from 'svelte';
	export let data: { id: string; value: string }[];
	const componentMap: Record<string, typeof SvelteComponent> = {
		Header,
		TextBox
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

{#each render_component() as { Component, props }}
	<svelte:component this={Component} content={props.content} />
{/each}
