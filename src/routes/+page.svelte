<script>
	const projects = [
		{
			title: 'Truss analysis workspace',
			status: 'Ready to deploy',
			description:
				'A focused engineering tool page for truss layouts, member forces, support reactions, and clear result summaries.',
			highlights: ['Input-friendly layout', 'Readable force tables', 'Export-ready results'],
			url: '#contact'
		},
		{
			title: 'Frame adjustment project',
			status: 'In progress',
			description:
				'A project slot for frame alignment, adjustment notes, before-and-after measurements, and deployment updates.',
			highlights: ['Adjustment log', 'Measurement checkpoints', 'Progress notes'],
			url: '#contact'
		},
		{
			title: 'Accessible web refresh',
			status: 'Live foundation',
			description:
				'The new site structure improves contrast, navigation, headings, focus states, and project discovery.',
			highlights: ['Semantic sections', 'Keyboard-friendly links', 'Mobile-first cards'],
			url: '#projects'
		}
	];
</script>

<svelte:head>
	<title>Amish Dahal | Engineering Projects</title>
	<meta
		name="description"
		content="Accessible portfolio and project list for truss, frame adjustment, and engineering web projects by Amish Dahal."
	/>
</svelte:head>

<section class="hero" aria-labelledby="page-title">
	<div class="hero-copy">
		<p class="eyebrow">Engineering portfolio</p>
		<h1 id="page-title">Build, document, and deploy structural project work clearly.</h1>
		<p class="intro">
			A cleaner home for Amish Dahal's projects, designed so visitors can quickly understand the
			work, open project details, and contact you about deployments.
		</p>
		<div class="hero-actions" aria-label="Primary actions">
			<a class="button primary" href="#projects">View projects</a>
			<a class="button secondary" href="https://github.com/AmishDahal">GitHub profile</a>
		</div>
	</div>

	<div class="hero-panel" aria-label="Project readiness summary">
		<div>
			<span class="metric">3</span>
			<span class="metric-label">project slots</span>
		</div>
		<div>
			<span class="metric">AA</span>
			<span class="metric-label">contrast target</span>
		</div>
		<div>
			<span class="metric">100%</span>
			<span class="metric-label">responsive layout</span>
		</div>
	</div>
</section>

<section class="section-block" id="projects" aria-labelledby="projects-title">
	<div class="section-heading">
		<p class="eyebrow">Project list</p>
		<h2 id="projects-title">Deployable workspaces</h2>
		<p>
			Use these cards as the main menu for your portfolio. Each item can later link to a live app,
			GitHub repo, report, or detailed project page.
		</p>
	</div>

	<div class="project-grid">
		{#each projects as project}
			<article class="project-card">
				<div class="card-topline">
					<h3>{project.title}</h3>
					<span>{project.status}</span>
				</div>
				<p>{project.description}</p>
				<ul aria-label={`${project.title} highlights`}>
					{#each project.highlights as highlight}
						<li>{highlight}</li>
					{/each}
				</ul>
				<a href={project.url}>Open project details</a>
			</article>
		{/each}
	</div>
</section>

<section class="section-block contact" id="contact" aria-labelledby="contact-title">
	<div>
		<p class="eyebrow">Next step</p>
		<h2 id="contact-title">Add your deployed links when they are ready.</h2>
		<p>
			When the truss or frame adjustment project is live, replace the card links with the deployed
			URLs. The page is already structured for screen readers, keyboard users, and small screens.
		</p>
	</div>
	<a class="button primary" href="mailto:amishdahal793@gmail.com">Contact Amish</a>
</section>

<style>
	:global(html) {
		scroll-behavior: smooth;
	}

	.hero,
	.section-block {
		width: 100%;
	}

	.hero {
		display: grid;
		grid-template-columns: 1fr;
		gap: 2rem;
		align-items: center;
		padding: 4rem 0 3rem;
	}

	.hero-copy {
		max-width: 44rem;
	}

	.eyebrow {
		margin: 0 0 0.75rem;
		color: #17675a;
		font-size: 0.8rem;
		font-weight: 700;
		letter-spacing: 0.08em;
		text-transform: uppercase;
	}

	h1,
	h2,
	h3,
	p {
		margin-top: 0;
	}

	h1 {
		max-width: 52rem;
		margin-bottom: 1rem;
		color: #10221f;
		font-size: clamp(2.25rem, 8vw, 4.8rem);
		font-weight: 800;
		line-height: 1;
		text-align: left;
	}

	h2 {
		margin-bottom: 0.75rem;
		color: #132825;
		font-size: 2rem;
		font-weight: 750;
		line-height: 1.1;
	}

	h3 {
		margin-bottom: 0;
		color: #132825;
		font-size: 1.15rem;
		font-weight: 750;
		line-height: 1.25;
	}

	.intro,
	.section-heading p,
	.contact p,
	.project-card p {
		color: #36524c;
		font-size: 1.05rem;
	}

	.hero-actions {
		display: flex;
		flex-wrap: wrap;
		gap: 0.75rem;
		margin-top: 1.5rem;
	}

	.button,
	.project-card a {
		display: inline-flex;
		align-items: center;
		justify-content: center;
		min-height: 2.75rem;
		border: 2px solid transparent;
		border-radius: 6px;
		padding: 0 1rem;
		font-weight: 750;
		text-decoration: none;
	}

	.button:focus-visible,
	.project-card a:focus-visible {
		outline: 3px solid #f2b705;
		outline-offset: 3px;
	}

	.primary {
		background: #17675a;
		color: #ffffff;
	}

	.secondary {
		border-color: #17675a;
		color: #17675a;
	}

	.hero-panel {
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		gap: 1px;
		overflow: hidden;
		border: 1px solid #c5d8d3;
		border-radius: 8px;
		background: #c5d8d3;
		box-shadow: 0 20px 50px rgb(16 34 31 / 12%);
	}

	.hero-panel > div {
		display: flex;
		min-height: 8rem;
		flex-direction: column;
		justify-content: center;
		padding: 1rem;
		background: #ffffff;
	}

	.metric {
		color: #17675a;
		font-size: 2rem;
		font-weight: 800;
		line-height: 1;
	}

	.metric-label {
		margin-top: 0.5rem;
		color: #4c625d;
		font-size: 0.9rem;
	}

	.section-block {
		padding: 3rem 0;
	}

	.section-heading {
		max-width: 42rem;
		margin-bottom: 1.5rem;
	}

	.project-grid {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(16rem, 1fr));
		gap: 1rem;
	}

	.project-card {
		display: flex;
		min-height: 22rem;
		flex-direction: column;
		border: 1px solid #c5d8d3;
		border-radius: 8px;
		padding: 1.25rem;
		background: #ffffff;
		box-shadow: 0 14px 35px rgb(16 34 31 / 8%);
	}

	.card-topline {
		display: grid;
		gap: 0.75rem;
	}

	.card-topline span {
		width: fit-content;
		border-radius: 999px;
		padding: 0.25rem 0.65rem;
		background: #e6f3ef;
		color: #17675a;
		font-size: 0.78rem;
		font-weight: 750;
	}

	.project-card ul {
		display: grid;
		gap: 0.5rem;
		margin: 0 0 1.5rem;
		padding-left: 1.1rem;
		color: #263f39;
	}

	.project-card a {
		margin-top: auto;
		background: #10221f;
		color: #ffffff;
	}

	.contact {
		display: grid;
		gap: 1rem;
		align-items: center;
		border-top: 1px solid #c5d8d3;
	}

	@media (min-width: 760px) {
		.hero {
			grid-template-columns: minmax(0, 1.35fr) minmax(18rem, 0.65fr);
			padding-top: 5rem;
		}

		.contact {
			grid-template-columns: 1fr auto;
		}
	}

	@media (max-width: 520px) {
		.hero {
			padding-top: 2.5rem;
		}

		.hero-panel {
			grid-template-columns: 1fr;
		}

		h1 {
			font-size: 2.45rem;
		}
	}
</style>
