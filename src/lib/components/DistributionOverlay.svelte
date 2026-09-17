<script>
	export let text = 'Coming Soon';
</script>

<div class="overlay">
	<div class="modal">
		<h1>{text}</h1>
		<p>Bigfoot Labs is currently under maintenance or being updated. Check back soon!</p>
	</div>
</div>

<style>
	.overlay {
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background-color: rgba(0, 0, 0, 0.85);
		backdrop-filter: blur(5px);
		z-index: 9999;
		display: flex;
		justify-content: center;
		align-items: center;
		color: white;
		font-family: sans-serif;
	}

	.modal {
		background-color: #222;
		padding: 2rem;
		border-radius: 12px;
		text-align: center;
		box-shadow: 0 4px 20px rgba(0, 0, 0, 0.5);
		border: 1px solid #444;
		max-width: 80%;
	}

	h1 {
		margin-top: 0;
		font-size: 2.5rem;
		color: #ff4500; /* Or a brand color */
		margin-bottom: 0.5rem;
		text-transform: uppercase;
		letter-spacing: 2px;
	}

	p {
		font-size: 1.1rem;
		color: #ddd;
	}
</style>
