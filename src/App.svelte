<script>
	let texto = '';
	let numero = 0;
	let rango = 0;
	let check = false;

	let frutas = ['tomate', 'palta', 'frutilla'];
	let radio = '';
	let arrayResultado = [];

</script>

<main class = "container">
	<h1>Bidings</h1>

	{#each frutas as fruta}
		<input type="radio" value={fruta} bind:group={radio}>
		{fruta}
	{/each}
	<p>fruta: {radio}</p>

	{#each frutas as fruta}
		<input type="checkbox" value={fruta} bind:group={arrayResultado}>
		{fruta}
	{/each}
	<p>arrayResultado: {arrayResultado}</p>

	<input type="checkbox" bind:checked={check}>
	<p>Aceptar políticas de la empresa</p>
	<button disabled={!check}>Enviar</button>
	<p>check: {check}</p>

	<input type="range" bind:value={rango} min="0" max="10">
	<p>rango: {rango}</p>

	<input type="number" bind:value={numero}>
	<p>numero: {numero}</p>

	<input type="text" bind:value={texto}>
	<p>texto: {texto}</p>
</main>

