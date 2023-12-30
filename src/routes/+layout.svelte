<script>
	import '../app.css';
	let asideVisible = false;
</script>

<main><slot /></main>
{#if asideVisible}
	<aside on:click={() => (asideVisible = false)}>
		<nav>
			<a href="#intro">Intro</a>
			<a href="#about">About Me</a>
			<a href="#infoblender">1. Infoblender</a>
			<a href="#mirkusve">3. Mirkusve</a>
			<a href="#fitquest">3. Fitquest</a>
			<a href="#spark">4. Spark</a>
			<a href="#achaye">5. Achaye</a>
			<a href="#worktogether">Let's Work together</a>
		</nav>
	</aside>
{:else}
	<button class="oswald" on:click={() => (asideVisible = true)}>Menu</button>
{/if}

<style>
	aside {
		min-height: 100vh;
		width: 100vw;

		position: fixed;
		top: 0;
		left: 0;
		backdrop-filter: blur(10px);

		display: flex;
	}

	a {
		padding: 1rem 2rem;
	}

	a:hover {
		background-color: white;
		color: black;
	}

	button {
		position: fixed;
		top: 1rem;
		left: 1rem;
		font-size: 1.5rem;
		backdrop-filter: blur(10px);
		padding: 10px 20px;
		border-radius: 10px;

	}

	nav {
		background-color: rgba(255, 255, 255, 0.205);
		display: flex;
		flex-direction: column;
		justify-content: center;
	}
</style>
