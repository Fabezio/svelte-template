<script>
	export let status;
	export let error;

	const dev = process.env.NODE_ENV === 'development';
</script>

<style>
	/* :root {
		background: rgba(255,69,0,0.2);
	} */
	h1, p {
		margin: 0 auto;
	}

	h1 {
		font-size: 2.8em;
		font-weight: 700;
		margin: 0 0 0.5em 0;
	}

	p {
		margin: 1em auto;
	}

	@media (min-width: 1200px) {
		h1 {
			font-size: 4em;
		}
	}

	.box {
		padding: 1rem 2rem;
		background: gold;
		color: orangered;
		border: 1px rgba(255,69,0,0.5) solid;
		border-radius: 2rem;
	}
	.shadow {
		text-shadow: 1px 1px darkslategrey;
	}
</style>

<svelte:head>
	<title>{status}</title>
</svelte:head>
<div class="box">
	
	<h1 class="shadow">{status}</h1>
	
	<p>{error.message}</p>
	
	{#if dev && error.stack}
		<pre>{error.stack}</pre>
	{/if}

</div>
