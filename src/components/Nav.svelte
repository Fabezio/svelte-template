<script>
	import Clock from "./Clock.svelte";
	import Links from "./Links.svelte"

	
	export let segment;
	

</script>

<style>
	nav {
		border-bottom: 1px solid rgba(255,62,0,0.1);
		font-weight: 300;
		padding: 0 1em;
	}

	ul {
		margin: 0;
		padding: 0;
	}

	/* clearfix */
	ul::after {
		content: '';
		display: block;
		clear: both;
	}

	li {
		display: block;
		float: left;
	}

	
	.float-right {
		float:right;
	}
	
</style>

<nav>
	<div>
		<ul>
			<li>
				<Links {segment} />

				
			</li>
				<ul>
					<li class="float-right">

						<Clock />
					</li>
				</ul>
			
		</ul>

	</div>
</nav>
