<script>
	import { frequency } from '../stores/frequency.js';
	import sightings from '../data/sightings.json';

	/** @type {{ name: string, summary: string, frequency: number } | undefined} */
	let currentSighting;

	// Subscribe to the store and update currentSighting based on the frequency
	$: currentSighting = sightings.find((s) => s.frequency === $frequency);
</script>

<div class="sighting-container">
	{#if currentSighting}
		<h2>{currentSighting.name}</h2>
		<p>{currentSighting.summary}</p>
	{:else}
		<p>No sighting record matches this frequency.</p>
	{/if}
</div>

<style>
	.sighting-container {
		border: 1px solid #ccc;
		padding: 1rem;
		border-radius: 8px;
		max-width: 600px;
		margin: 1rem auto;
		background-color: #f9f9f9;
        font-family: sans-serif;
	}

	h2 {
		margin-top: 0;
		color: #333;
	}

	p {
		color: #555;
		line-height: 1.5;
	}
</style>
