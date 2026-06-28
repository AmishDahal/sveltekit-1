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
		<p>Amish Dahal / movies, engineering ideas, web projects, and unfinished builds.</p>
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
		border-top: 1px solid rgb(255 255 255 / 10%);
		padding: 1.5rem 1rem;
		color: #9ca3af;
		text-align: center;
	}

	footer p {
		margin: 0;
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
