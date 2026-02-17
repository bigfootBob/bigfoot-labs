
<script>
	import SightingDisplay from '../lib/components/SightingDisplay.svelte';
	import { frequency } from '../lib/stores/frequency.js';

	/**
	 * @param {Event} event
	 */
	function handleFrequencyChange(event) {
		// @ts-ignore
		frequency.set(Number(event.target.value));
	}
</script>

<h1>Bigfoot Labs - Cryptid Frequency Tuner</h1>

<div class="controls">
	<label for="frequency">Tuning Frequency: {$frequency}</label>
	<input
		type="range"
		id="frequency"
		min="1"
		max="5"
		step="1"
		value={$frequency}
		on:input={handleFrequencyChange}
	/>
</div>

<SightingDisplay />

<style>
	:global(body) {
		font-family: Arial, sans-serif;
		padding: 2rem;
		background-color: #f0f2f5;
	}

	h1 {
		text-align: center;
		color: #2c3e50;
	}

	.controls {
		margin: 2rem auto;
		text-align: center;
		max-width: 400px;
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 1rem;
	}

	label {
		font-weight: bold;
		color: #555;
	}

	input[type='range'] {
		width: 100%;
		cursor: pointer;
	}
</style>
