<script>
	let name = 'Judith';
	let shoecolour = 'black';

	const handleCLick = () => {
		shoecolour = 'red';
	};
	const handleInput = (e) => {
		shoecolour = e.target.value 
	};
</script>

<main>
	<h1>Hello {name}!</h1>
	<p style="color: {shoecolour}">{shoecolour} shoe</p>
	<button on:click={handleCLick}> update shoe clour</button>
	<!-- <input type="text" on:input={handleInput} value={shoecolour}> -->
	 <input type="text" bind:value={shoecolour}>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>