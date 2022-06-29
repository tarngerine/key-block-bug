<script lang="ts">
	import { onMount } from 'svelte';
	import { fade } from 'svelte/transition';

	let index = 0;
	onMount(() => {
		setInterval(() => {
			index++;
		}, 1000);
	});
</script>

{#key index}
	<div transition:fade>Key {index}</div>
{/key}
