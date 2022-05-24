<script>
	import '../app.css';
</script>

<div class="base-layout layout">
	<header>
		<a class="logo" href="/">Sports Concussions</a>
		<nav>
			<ul>
				<li><a href="/works-cited/">Works Cited</a></li>
			</ul>
		</nav>
	</header>
	<main id="content">
		<slot />
	</main>
	<footer>
		<div class="logo">Sports Concussions<br /><small>Clayton Kruse</small></div>
		<ul>
			<li><a href="/">Home</a></li>
		</ul>
	</footer>
</div>

<style>
	.layout {
		min-height: 100vh;
		color: black;
		background-color: hsl(0, 0%, 90%);

		--gutter: 8vw;

		display: flex;
		flex-flow: column;

		font-family: var(--font-sans);
	}

	header {
		padding: 0 var(--gutter);
		display: flex;
		flex-wrap: wrap;
		background-color: var(--theme-primary);
	}

	header nav {
		display: flex;
	}

	header nav ul {
		list-style: none;
		padding: 0;
		display: flex;
		flex-wrap: wrap;
		align-content: center;
		align-items: center;
	}

	header nav ul li {
		padding: 0.2em;
	}

	header nav a {
		color: inherit;
		font-weight: bold;
		text-transform: uppercase;
	}

	main {
		background-color: hsl(0, 0%, 95%);
		margin: 0.5em var(--gutter);
		padding: 2em;
		flex-grow: 1;

		font-family: var(--font-serif);
	}

	footer {
		display: flex;
		margin-top: auto;
		padding: 0.3em var(--gutter);
		background-color: hsl(0, 0%, 6%);
		color: white;
	}

	.logo {
		font-weight: bold;
		color: inherit;
		margin-right: 1rem;
		text-decoration: none;
	}
	header .logo {
		font-size: 1.5em;
		height: 3rem;
		display: flex;
		align-items: center;
	}
</style>
