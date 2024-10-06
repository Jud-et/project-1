<script>
	let people = [
		{name: 'judith', shoecolour: 'red', age: 20, id: 1},
		{name: 'Doreen', shoecolour: 'blue', age: 18, id: 2},
		{name: 'Felix', shoecolour: 'black', age: 22, id: 3}
	];

</script>

<main>
	{#each people as person (person.id)}
	<div>
		<h4>{person.name} </h4>
		<p>{person.age} years old, {person.shoecolour} shoe </p>
	</div>
	{:else}
	<p>There are no people to show...</p>

	{/each}
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