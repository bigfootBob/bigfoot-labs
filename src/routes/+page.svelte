<script>
	// No script needed for this simple navigation view
</script>

<h1>Bigfoot Labs</h1>

<div class="grid-container">
	<a href="/tuner" class="tile tuner">
		<h2>Tuner</h2>
		<p>Cryptid Frequency Tuner</p>
	</a>
	<a href="/game" class="tile game">
		<h2>Game</h2>
		<p>Play the Game</p>
	</a>
	<a href="/experiment" class="tile experiment">
		<h2>Experiment</h2>
		<p>Lab Experiments</p>
	</a>
	<a href="/erotica" class="tile erotica">
		<h2>Choose your own squatch</h2>
		<p>Sensual Sasquatch Stories</p>
	</a>
</div>

<style>
	:global(body) {
		font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
		background-color: #1a1a1a;
		color: #fff;
		margin: 0;
		padding: 2rem;
	}

	h1 {
		text-align: center;
		margin-bottom: 3rem;
		font-size: 3rem;
		color: #ddd;
	}

	.grid-container {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
		gap: 2rem;
		max-width: 1200px;
		margin: 0 auto;
	}

	.tile {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 3rem;
		border-radius: 12px;
		text-decoration: none;
		color: white;
		transition:
			transform 0.2s,
			box-shadow 0.2s;
		min-height: 200px;
		text-align: center;
	}

	.tile:hover {
		transform: translateY(-5px);
		box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
	}

	.tile h2 {
		margin: 0 0 0.5rem 0;
		font-size: 2rem;
	}

	.tile p {
		margin: 0;
		opacity: 0.8;
	}

	/* Distinct colors for each tile */
	.tuner {
		background: linear-gradient(135deg, #ff6b6b, #ee5253);
	}

	.game {
		background: linear-gradient(135deg, #48dbfb, #0abde3);
	}

	.experiment {
		background: linear-gradient(135deg, #1dd1a1, #10ac84);
	}

	.erotica {
		background: linear-gradient(135deg, #ff9ff3, #f368e0);
	}
</style>
