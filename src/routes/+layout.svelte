<script>
	import favicon from '$lib/assets/favicon.svg';
	import { DISTRIBUTION_MODE } from '$lib/index.js';
	import DistributionOverlay from '$lib/components/DistributionOverlay.svelte';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

{#if DISTRIBUTION_MODE}
	<DistributionOverlay />
{/if}

{@render children()}
