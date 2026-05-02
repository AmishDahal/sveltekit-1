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
				<a href="/#projects">Projects</a>
			</li>
			<li>
				<a href="/#contact">Contact</a>
			</li>
		</ul>
	</nav>
</header>

<style>
	header {
		display: flex;
		flex-wrap: wrap;
		gap: 1rem;
		align-items: center;
		justify-content: space-between;
		padding: 1rem;
		border-bottom: 1px solid rgb(23 103 90 / 16%);
		background: rgb(255 255 255 / 82%);
		backdrop-filter: blur(14px);
	}

	.skip-link {
		position: absolute;
		left: 1rem;
		top: 0.5rem;
		z-index: 10;
		transform: translateY(-150%);
		border-radius: 6px;
		padding: 0.65rem 0.85rem;
		background: #10221f;
		color: #ffffff;
		font-weight: 750;
		text-decoration: none;
	}

	.skip-link:focus {
		transform: translateY(0);
	}

	.brand {
		display: flex;
		align-items: center;
		gap: 0.7rem;
		color: #10221f;
		text-decoration: none;
	}

	.brand span {
		display: inline-flex;
		width: 2.5rem;
		height: 2.5rem;
		align-items: center;
		justify-content: center;
		border-radius: 8px;
		background: #17675a;
		color: #ffffff;
		font-weight: 800;
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

	li {
		position: relative;
	}

	nav a {
		display: flex;
		align-items: center;
		min-height: 2.5rem;
		border-radius: 6px;
		padding: 0 0.8rem;
		color: #263f39;
		font-weight: 700;
		text-decoration: none;
	}

	li[aria-current='page'] a,
	nav a:hover {
		background: #e6f3ef;
		color: #17675a;
		text-decoration: none;
	}

	a:focus-visible {
		outline: 3px solid #f2b705;
		outline-offset: 3px;
	}

	@media (min-width: 720px) {
		header {
			padding: 1rem 2rem;
		}
	}
</style>
