<script>
	import { browser } from '$app/environment';
	import { page } from '$app/stores';
	import { webVitals } from '$lib/vitals';
	import Header from './Header.svelte';
	import './styles.css';

	/** @type {import('./$types').LayoutServerData} */
	export let data;

	$: if (browser && data?.analyticsId) {
		webVitals({
			path: $page.url.pathname,
			params: $page.params,
			analyticsId: data.analyticsId
		});
	}
</script>

<div class="app">
	<Header />

	<main id="main-content" tabindex="-1">
		<slot />
	</main>

	<footer>
		<p>Portfolio of Amish Dahal: projects, interests, and things still in progress.</p>
	</footer>
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 0 1rem;
		width: 100%;
		max-width: 72rem;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 1.5rem 1rem;
		color: #4c625d;
		text-align: center;
	}

	main:focus {
		outline: none;
	}

	@media (min-width: 480px) {
		footer {
			padding: 1.5rem 0;
		}

		main {
			padding-inline: 2rem;
		}
	}
</style>
