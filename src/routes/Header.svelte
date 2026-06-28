<script>
	import { page } from '$app/stores';
</script>

<header>
	<a class="skip-link" href="#main-content">Skip to content</a>
	<a class="brand" href="/" aria-label="Amish Dahal home">
		<span aria-hidden="true">AD</span>
		<strong>Amish Dahal</strong>
	</a>

	<nav aria-label="Main navigation">
		<ul>
			<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
				<a href="/">Home</a>
			</li>
			<li>
				<a href="/#about">About</a>
			</li>
			<li>
				<a href="/#interests">Interests</a>
			</li>
			<li>
				<a href="/#projects">Projects</a>
			</li>
			<li>
				<a class="launch-link" href="/structure-lab.html">Structure Lab</a>
			</li>
		</ul>
	</nav>
</header>

<style>
	header {
		position: sticky;
		top: 0;
		z-index: 20;
		display: flex;
		flex-wrap: wrap;
		gap: 1rem;
		align-items: center;
		justify-content: space-between;
		padding: 0.85rem 1rem;
		border-bottom: 1px solid rgb(255 255 255 / 10%);
		background: rgb(9 11 16 / 82%);
		backdrop-filter: blur(18px);
	}

	.skip-link {
		position: absolute;
		left: 1rem;
		top: 0.5rem;
		z-index: 30;
		transform: translateY(-150%);
		border-radius: 6px;
		padding: 0.65rem 0.85rem;
		background: #f4b35e;
		color: #111827;
		font-weight: 850;
		text-decoration: none;
	}

	.skip-link:focus {
		transform: translateY(0);
	}

	.brand {
		display: flex;
		align-items: center;
		gap: 0.7rem;
		color: #ffffff;
		text-decoration: none;
	}

	.brand span {
		display: inline-flex;
		width: 2.45rem;
		height: 2.45rem;
		align-items: center;
		justify-content: center;
		border: 1px solid rgb(244 179 94 / 70%);
		border-radius: 8px;
		background: rgb(244 179 94 / 14%);
		color: #f4b35e;
		font-weight: 900;
	}

	.brand strong {
		font-size: 1rem;
		line-height: 1;
	}

	nav {
		display: flex;
		justify-content: center;
	}

	ul {
		display: flex;
		flex-wrap: wrap;
		gap: 0.35rem;
		align-items: center;
		padding: 0;
		margin: 0;
		list-style: none;
	}

	nav a {
		display: flex;
		align-items: center;
		min-height: 2.35rem;
		border-radius: 8px;
		padding: 0 0.78rem;
		color: #d1d5db;
		font-size: 0.92rem;
		font-weight: 760;
		text-decoration: none;
	}

	li[aria-current='page'] a,
	nav a:hover {
		background: rgb(255 255 255 / 9%);
		color: #ffffff;
		text-decoration: none;
	}

	nav a.launch-link {
		background: #f4b35e;
		color: #111827;
	}

	a:focus-visible {
		outline: 3px solid #67e8f9;
		outline-offset: 3px;
	}

	@media (min-width: 720px) {
		header {
			padding: 0.85rem 2rem;
		}
	}
</style>
