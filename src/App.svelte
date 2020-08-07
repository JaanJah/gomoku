<script lang="ts">
	import Playfield from './Playfield.svelte';
	import { onMount } from 'svelte';

	let playfield;

	onMount(() => {
		playfield.createPlayfield();
		playfield.createClickableDOM();
	})
</script>
<main>
 <Playfield bind:this={playfield}/>
</main>