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
		display: flex;
		flex-wrap: wrap;
		gap: 1rem;
		align-items: center;
		justify-content: space-between;
		padding: 1rem;
		border-bottom: 1px solid rgb(31 111 120 / 16%);
		background: rgb(255 255 255 / 88%);
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
		background: #151515;
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
		color: #151515;
		text-decoration: none;
	}

	.brand span {
		display: inline-flex;
		width: 2.5rem;
		height: 2.5rem;
		align-items: center;
		justify-content: center;
		border-radius: 8px;
		background: #1f6f78;
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
		background: #eef3f5;
		color: #1f6f78;
		text-decoration: none;
	}

	nav a.launch-link {
		background: #1f6f78;
		color: #ffffff;
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
