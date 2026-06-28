<svelte:head>
	<title>Amish Dahal | Portfolio</title>
	<meta
		name="description"
		content="Portfolio of Amish Dahal, featuring interests in movies, engineering, web projects, and unfinished work like Structure Lab."
	/>
</svelte:head>

<section class="hero" aria-labelledby="page-title">
	<div class="hero-copy">
		<p class="eyebrow">Portfolio</p>
		<h1 id="page-title">Amish Dahal</h1>
		<p class="intro">
			I am building this place as a personal portfolio for what I make, what I am learning,
			and what I am interested in. I like movies, visual ideas, and small projects that slowly
			become better with time.
		</p>
		<div class="hero-actions" aria-label="Primary actions">
			<a class="button primary" href="#projects">Projects</a>
			<a class="button secondary" href="#interests">Interests</a>
		</div>
	</div>

	<aside class="social-card" aria-label="Social links">
		<div class="avatar" aria-hidden="true">AD</div>
		<p class="card-kicker">Find me online</p>
		<div class="social-links">
			<a href="https://www.facebook.com/amishdahal69" rel="noreferrer" target="_blank">Facebook</a>
			<a href="https://www.instagram.com/amish_dahal/" rel="noreferrer" target="_blank">Instagram</a>
		</div>
	</aside>
</section>

<section class="section-block" id="about" aria-labelledby="about-title">
	<div class="section-heading">
		<p class="eyebrow">About</p>
		<h2 id="about-title">A simple page for my interests, experiments, and progress.</h2>
		<p>
			This portfolio is not meant to look finished forever. It is a place where I can show
			what I am learning, keep track of projects, and share the things that shape my taste,
			from engineering explanations to movies and creative media.
		</p>
	</div>
</section>

<section class="section-block" id="interests" aria-labelledby="interests-title">
	<div class="section-heading">
		<p class="eyebrow">Interests</p>
		<h2 id="interests-title">Things I keep coming back to.</h2>
	</div>

	<div class="interest-grid">
		<article>
			<h3>Movies</h3>
			<p>
				I like movies because they mix story, mood, characters, music, and visuals into one
				experience. Good films stay in your head after they end.
			</p>
		</article>
		<article>
			<h3>Engineering ideas</h3>
			<p>
				I enjoy making hard concepts easier to understand with diagrams, examples, and clear
				visual explanations.
			</p>
		</article>
		<article>
			<h3>Web projects</h3>
			<p>
				I like turning rough ideas into usable pages and tools, then improving them step by step
				as I learn more.
			</p>
		</article>
	</div>
</section>

<section class="section-block socials" aria-labelledby="socials-title">
	<div class="section-heading">
		<p class="eyebrow">Socials</p>
		<h2 id="socials-title">More of what I share and repost.</h2>
		<p>
			My public social profiles are linked here so visitors can see more of my taste,
			updates, and reposts outside this portfolio.
		</p>
	</div>
	<div class="social-list">
		<a href="https://www.facebook.com/amishdahal69" rel="noreferrer" target="_blank">Facebook</a>
		<a href="https://www.instagram.com/amish_dahal/" rel="noreferrer" target="_blank">Instagram</a>
	</div>
</section>

<section class="section-block" id="projects" aria-labelledby="projects-title">
	<div class="section-heading">
		<p class="eyebrow">Projects</p>
		<h2 id="projects-title">Projects I am still shaping.</h2>
		<p>
			The previous main project has been moved here so the homepage can be about me first,
			while the project still has its own space.
		</p>
	</div>

	<article class="project-card">
		<div class="project-copy">
			<div class="project-labels">
				<span class="status-tag">Unfinished</span>
				<span>Structure Lab</span>
			</div>
			<h3>A visual study tool for AFD, SFD, and BMD.</h3>
			<p>
				Structure Lab is a student-friendly structural mechanics project for learning free body
				diagrams, axial force diagrams, shear force diagrams, bending moment diagrams, and
				tension or compression in members.
			</p>
			<a class="text-link" href="/structure-lab.html">Open Structure Lab</a>
		</div>

		<div class="lab-preview" aria-label="Structure Lab diagram preview">
			<div class="preview-header"><span></span><span></span><span></span><strong>AFD / SFD / BMD</strong></div>
			<svg viewBox="0 0 680 420" role="img" aria-label="Structural diagram preview">
				<path class="grid" d="M60 340H620M60 270H620M60 200H620M60 130H620M140 70V360M260 70V360M380 70V360M500 70V360" />
				<path class="member compression" d="M90 330H590" />
				<path class="member frame" d="M130 330V135H330V330" />
				<path class="member tension" d="M330 330L460 150L590 330M330 330H590M460 150H590" />
				<path class="deflected" d="M130 334C178 265 225 145 330 139C355 215 405 274 460 160C505 236 548 300 590 336" />
				<g class="load"><path d="M460 58V128" /><path d="M460 128l-13-23M460 128l13-23" /></g>
				<g class="nodes"><circle cx="90" cy="330" r="9" /><circle cx="130" cy="330" r="9" /><circle cx="130" cy="135" r="9" /><circle cx="330" cy="135" r="9" /><circle cx="330" cy="330" r="9" /><circle cx="460" cy="150" r="9" /><circle cx="590" cy="330" r="9" /></g>
				<text x="86" y="382">support reactions</text><text x="360" y="48">load</text><text x="430" y="382">tension / compression</text>
			</svg>
		</div>
	</article>
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
		padding: 4.5rem 0 3rem;
	}

	.hero-copy,
	.section-heading {
		max-width: 48rem;
	}

	.eyebrow,
	.card-kicker,
	.project-labels {
		margin: 0 0 0.75rem;
		color: #9a3412;
		font-size: 0.8rem;
		font-weight: 850;
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
		max-width: 54rem;
		margin-bottom: 1rem;
		color: #151515;
		font-size: clamp(3rem, 9vw, 6rem);
		font-weight: 850;
		line-height: 0.95;
		text-align: left;
	}

	h2 {
		margin-bottom: 0.8rem;
		color: #151515;
		font-size: clamp(2rem, 4vw, 3.15rem);
		font-weight: 800;
		line-height: 1.06;
	}

	h3 {
		margin-bottom: 0.7rem;
		color: #1c2430;
		font-size: 1.15rem;
		font-weight: 800;
	}

	.intro,
	.section-heading p,
	.interest-grid p,
	.project-card p {
		color: #4d5965;
		font-size: 1.08rem;
		line-height: 1.65;
	}

	.hero-actions,
	.social-links,
	.social-list,
	.project-labels {
		display: flex;
		flex-wrap: wrap;
		gap: 0.75rem;
		align-items: center;
	}

	.hero-actions {
		margin-top: 1.6rem;
	}

	.button,
	.social-links a,
	.social-list a {
		display: inline-flex;
		align-items: center;
		justify-content: center;
		min-height: 2.85rem;
		border: 2px solid transparent;
		border-radius: 8px;
		padding: 0 1.1rem;
		font-weight: 800;
		text-decoration: none;
	}

	.primary,
	.social-links a:first-child,
	.social-list a:first-child {
		background: #1f6f78;
		color: #ffffff;
	}

	.secondary,
	.social-links a:last-child,
	.social-list a:last-child {
		border-color: #1f6f78;
		background: #ffffff;
		color: #1f6f78;
	}

	.button:focus-visible,
	.text-link:focus-visible,
	.social-links a:focus-visible,
	.social-list a:focus-visible {
		outline: 3px solid #f2b705;
		outline-offset: 3px;
	}

	.social-card,
	.interest-grid article,
	.project-card {
		border: 1px solid #d6dde5;
		border-radius: 8px;
		background: #ffffff;
		box-shadow: 0 18px 45px rgb(24 32 42 / 8%);
	}

	.social-card {
		padding: 1.4rem;
	}

	.avatar {
		display: grid;
		width: 5.25rem;
		height: 5.25rem;
		margin-bottom: 1.2rem;
		place-items: center;
		border-radius: 8px;
		background: #1f6f78;
		color: #ffffff;
		font-size: 1.6rem;
		font-weight: 850;
	}

	.section-block {
		padding: 3.75rem 0;
		border-top: 1px solid #d6dde5;
	}

	.section-heading {
		margin-bottom: 1.5rem;
	}

	.interest-grid {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(16rem, 1fr));
		gap: 1rem;
	}

	.interest-grid article {
		min-height: 13rem;
		padding: 1.25rem;
	}

	.socials {
		display: grid;
		gap: 1rem;
		align-items: center;
	}

	.project-card {
		display: grid;
		gap: 1.35rem;
		padding: 1.25rem;
	}

	.project-labels {
		text-transform: none;
	}

	.status-tag {
		display: inline-flex;
		align-items: center;
		min-height: 1.75rem;
		border: 1px solid #f59e0b;
		border-radius: 999px;
		padding: 0 0.7rem;
		background: #fff7ed;
		color: #9a3412;
		font-size: 0.78rem;
		font-weight: 850;
		text-transform: uppercase;
	}

	.text-link {
		display: inline-flex;
		margin-top: 0.35rem;
		color: #1f6f78;
		font-weight: 850;
		text-underline-offset: 0.2em;
	}

	.lab-preview {
		overflow: hidden;
		border: 1px solid #cbd6de;
		border-radius: 8px;
		background: #ffffff;
	}

	.preview-header {
		display: flex;
		align-items: center;
		gap: 0.45rem;
		height: 2.75rem;
		padding: 0 1rem;
		border-bottom: 1px solid #d9e1e7;
		background: #eef3f5;
		color: #40505e;
		font-size: 0.82rem;
	}

	.preview-header span {
		width: 0.65rem;
		height: 0.65rem;
		border-radius: 50%;
		background: #9aa7b4;
	}

	.preview-header strong {
		margin-left: 0.35rem;
	}

	svg {
		display: block;
		width: 100%;
		height: auto;
		background: #fbfcfd;
	}

	.grid {
		fill: none;
		stroke: #e4eaf0;
		stroke-width: 1;
	}

	.member,
	.deflected,
	.load path {
		fill: none;
		stroke-linecap: round;
		stroke-linejoin: round;
	}

	.member {
		stroke-width: 12;
	}

	.compression {
		stroke: #cb3b3b;
	}

	.frame {
		stroke: #7154b8;
	}

	.tension {
		stroke: #1f8a5b;
	}

	.deflected {
		stroke: #111827;
		stroke-dasharray: 10 8;
		stroke-width: 4;
	}

	.load path {
		stroke: #1f6f78;
		stroke-width: 7;
	}

	.nodes circle {
		fill: #ffffff;
		stroke: #111827;
		stroke-width: 4;
	}

	svg text {
		fill: #52616f;
		font: 700 18px system-ui;
	}

	@media (min-width: 820px) {
		.hero {
			grid-template-columns: minmax(0, 1fr) minmax(22rem, 0.55fr);
			padding-top: 5.25rem;
		}

		.social-card {
			padding: 1.7rem;
		}

		.socials {
			grid-template-columns: 1fr auto;
		}

		.project-card {
			grid-template-columns: minmax(0, 0.8fr) minmax(24rem, 1fr);
			align-items: center;
			padding: 1.5rem;
		}
	}

	@media (max-width: 560px) {
		.hero {
			padding-top: 2.5rem;
		}

		h1 {
			font-size: 3rem;
		}
	}
</style>
