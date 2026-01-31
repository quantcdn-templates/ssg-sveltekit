<script lang="ts">
	import type { Snippet } from 'svelte';

	let { children }: { children: Snippet } = $props();
</script>

<svelte:head>
	<title>SvelteKit on QuantCDN</title>
	<meta name="description" content="SvelteKit static site template for QuantCDN" />
</svelte:head>

{@render children()}

<style>
	:global(html, body) {
		margin: 0;
		padding: 0;
		font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell,
			'Fira Sans', 'Droid Sans', 'Helvetica Neue', sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		background-color: #f5f5f5;
		color: #333;
	}

	:global(*) {
		box-sizing: border-box;
	}

	:global(a) {
		color: #ff3e00;
		text-decoration: none;
	}

	:global(a:hover) {
		text-decoration: underline;
	}
</style>
