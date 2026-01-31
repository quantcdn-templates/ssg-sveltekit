<script lang="ts">
	let count = $state(0);

	function increment() {
		count += 1;
	}
</script>

<main>
	<div class="hero">
		<img src="/svelte-logo.svg" alt="Svelte Logo" class="logo" />
		<h1>Welcome to SvelteKit</h1>
		<p class="tagline">Deployed on QuantCDN</p>
	</div>

	<section class="demo">
		<h2>Interactive Counter</h2>
		<p>This demonstrates Svelte's reactivity:</p>
		<button onclick={increment}>
			Clicks: {count}
		</button>
	</section>

	<section class="features">
		<h2>Features</h2>
		<ul>
			<li>Static site generation with <code>@sveltejs/adapter-static</code></li>
			<li>TypeScript support out of the box</li>
			<li>Svelte 5 with runes</li>
			<li>Automatic deployment to QuantCDN</li>
			<li>Global CDN distribution</li>
		</ul>
	</section>

	<section class="links">
		<h2>Resources</h2>
		<ul>
			<li><a href="https://svelte.dev/docs/kit" target="_blank" rel="noopener">SvelteKit Documentation</a></li>
			<li><a href="https://svelte.dev/docs/svelte" target="_blank" rel="noopener">Svelte Documentation</a></li>
			<li><a href="https://www.quantcdn.io/docs" target="_blank" rel="noopener">QuantCDN Documentation</a></li>
		</ul>
	</section>
</main>

<style>
	main {
		max-width: 800px;
		margin: 0 auto;
		padding: 2rem;
	}

	.hero {
		text-align: center;
		padding: 3rem 0;
	}

	.logo {
		width: 120px;
		height: 120px;
		margin-bottom: 1rem;
	}

	h1 {
		font-size: 2.5rem;
		margin: 0 0 0.5rem;
		color: #ff3e00;
	}

	.tagline {
		font-size: 1.25rem;
		color: #666;
		margin: 0;
	}

	section {
		background: white;
		border-radius: 8px;
		padding: 1.5rem;
		margin-bottom: 1.5rem;
		box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
	}

	h2 {
		margin-top: 0;
		color: #333;
	}

	.demo {
		text-align: center;
	}

	button {
		background: #ff3e00;
		color: white;
		border: none;
		padding: 0.75rem 1.5rem;
		font-size: 1.125rem;
		border-radius: 4px;
		cursor: pointer;
		transition: background-color 0.2s;
	}

	button:hover {
		background: #e63600;
	}

	button:active {
		background: #cc3000;
	}

	ul {
		padding-left: 1.5rem;
	}

	li {
		margin-bottom: 0.5rem;
	}

	code {
		background: #f0f0f0;
		padding: 0.125rem 0.375rem;
		border-radius: 3px;
		font-size: 0.9em;
	}
</style>
