<svelte:head>
	<title>Amish Dahal | Portfolio</title>
	<meta
		name="description"
		content="A cinematic personal portfolio for Amish Dahal with interests in movies, visual engineering, web projects, and Structure Lab."
	/>
</svelte:head>

<section class="hero" aria-labelledby="page-title">
	<img
		class="hero-image"
		src="https://images.unsplash.com/photo-1489599849927-2ee91cede3ba?auto=format&fit=crop&w=1800&q=85"
		alt="Rows of cinema seats facing a glowing movie screen"
	/>
	<div class="hero-shade"></div>
	<div class="hero-content">
		<p class="eyebrow">Portfolio / movies / engineering / web</p>
		<h1 id="page-title">Amish Dahal</h1>
		<p class="intro">
			A personal space for the things I make and the things I like: cinematic stories,
			visual explanations, unfinished experiments, and small web projects that keep getting better.
		</p>
		<div class="hero-actions" aria-label="Primary actions">
			<a class="button primary" href="#projects">See projects</a>
			<a class="button secondary" href="https://www.instagram.com/amish_dahal/" rel="noreferrer" target="_blank">Instagram</a>
			<a class="button ghost" href="https://www.facebook.com/amishdahal69" rel="noreferrer" target="_blank">Facebook</a>
		</div>
	</div>
	<div class="hero-strip" aria-hidden="true">
		<span>Films</span>
		<span>Visual ideas</span>
		<span>Learning by building</span>
	</div>
</section>

<section class="section-block intro-block" id="about" aria-labelledby="about-title">
	<div class="section-heading">
		<p class="eyebrow">About</p>
		<h2 id="about-title">Not a boring resume page. More like a place to collect taste, work, and progress.</h2>
	</div>
	<p>
		I am using this portfolio to show what I am interested in and what I am building. The
		center of it is simple: movies and visual storytelling on one side, engineering and web
		tools on the other. Some things here are finished, some are rough, and the rough ones are
		part of the point.
	</p>
</section>

<section class="section-block" id="interests" aria-labelledby="interests-title">
	<div class="section-heading wide">
		<p class="eyebrow">Interests</p>
		<h2 id="interests-title">The mix.</h2>
	</div>

	<div class="interest-grid">
		<article class="interest-card movie-card">
			<img
				src="https://images.unsplash.com/photo-1485846234645-a62644f84728?auto=format&fit=crop&w=1100&q=85"
				alt="Movie production camera in a dark scene"
			/>
			<div>
				<span>01</span>
				<h3>Movies</h3>
				<p>Stories, atmosphere, characters, music, shots, edits: movies are the interest that gives the page its mood.</p>
			</div>
		</article>

		<article class="interest-card">
			<img
				src="https://images.unsplash.com/photo-1503387762-592deb58ef4e?auto=format&fit=crop&w=1100&q=85"
				alt="Architectural structure with strong lines and geometry"
			/>
			<div>
				<span>02</span>
				<h3>Engineering ideas</h3>
				<p>I like concepts that become easier when they are drawn clearly: forces, diagrams, structure, and cause-effect thinking.</p>
			</div>
		</article>

		<article class="interest-card web-card">
			<img
				src="https://images.unsplash.com/photo-1498050108023-c5249f4df085?auto=format&fit=crop&w=1100&q=85"
				alt="Laptop showing code on a desk"
			/>
			<div>
				<span>03</span>
				<h3>Web projects</h3>
				<p>Small pages, tools, experiments, broken ideas that slowly turn into better ones. That is the fun part.</p>
			</div>
		</article>
	</div>
</section>

<section class="section-block socials" aria-labelledby="socials-title">
	<div class="section-heading">
		<p class="eyebrow">Socials</p>
		<h2 id="socials-title">More of the taste outside the site.</h2>
		<p>Follow the public profiles for posts, reposts, updates, and whatever I am into lately.</p>
	</div>
	<div class="social-list">
		<a href="https://www.instagram.com/amish_dahal/" rel="noreferrer" target="_blank">Instagram</a>
		<a href="https://www.facebook.com/amishdahal69" rel="noreferrer" target="_blank">Facebook</a>
	</div>
</section>

<section class="section-block" id="projects" aria-labelledby="projects-title">
	<div class="section-heading wide">
		<p class="eyebrow">Projects</p>
		<h2 id="projects-title">The build log.</h2>
		<p>The old homepage project now lives here, where it belongs: as one project inside the wider portfolio.</p>
	</div>

	<article class="project-card">
		<div class="project-media">
			<img
				src="https://images.unsplash.com/photo-1581091215367-59ab6b8e8a88?auto=format&fit=crop&w=1300&q=85"
				alt="Engineering workspace with technical tools and plans"
			/>
			<span class="status-tag">Unfinished</span>
		</div>
		<div class="project-copy">
			<p class="eyebrow">Structure Lab</p>
			<h3>A visual study tool for AFD, SFD, and BMD.</h3>
			<p>
				Structure Lab is a student-friendly structural mechanics project for learning free body
				diagrams, axial force diagrams, shear force diagrams, bending moment diagrams, and
				tension or compression in members.
			</p>
			<a class="button primary" href="/structure-lab.html">Open Structure Lab</a>
		</div>
	</article>
</section>

<style>
	:global(html) {
		scroll-behavior: smooth;
	}

	.hero {
		position: relative;
		min-height: min(760px, calc(100vh - 4.5rem));
		display: grid;
		align-items: end;
		isolation: isolate;
		overflow: hidden;
		border-radius: 0 0 8px 8px;
		margin-inline: calc(50% - 50vw);
		padding: clamp(4rem, 10vw, 7rem) max(1rem, calc((100vw - 72rem) / 2)) 2rem;
		background: #090b10;
	}

	.hero-image,
	.hero-shade {
		position: absolute;
		inset: 0;
		width: 100%;
		height: 100%;
	}

	.hero-image {
		z-index: -3;
		object-fit: cover;
	}

	.hero-shade {
		z-index: -2;
		background:
			linear-gradient(90deg, rgb(5 8 13 / 95%) 0%, rgb(5 8 13 / 72%) 43%, rgb(5 8 13 / 28%) 100%),
			linear-gradient(0deg, #090b10 0%, rgb(9 11 16 / 0%) 42%);
	}

	.hero-content {
		max-width: 58rem;
		padding-bottom: clamp(2rem, 6vw, 5rem);
	}

	.eyebrow {
		margin: 0 0 0.85rem;
		color: #f4b35e;
		font-size: 0.78rem;
		font-weight: 850;
		letter-spacing: 0.14em;
		text-transform: uppercase;
	}

	h1,
	h2,
	h3,
	p {
		margin-top: 0;
	}

	h1 {
		max-width: 11ch;
		margin-bottom: 1rem;
		color: #ffffff;
		font-size: clamp(4rem, 14vw, 10.5rem);
		font-weight: 900;
		line-height: 0.84;
		text-align: left;
	}

	h2 {
		margin-bottom: 1rem;
		color: #fff8ed;
		font-size: clamp(2.4rem, 6vw, 5rem);
		font-weight: 900;
		line-height: 0.95;
	}

	h3 {
		margin-bottom: 0.8rem;
		color: #ffffff;
		font-size: clamp(1.55rem, 3vw, 2.6rem);
		font-weight: 850;
		line-height: 1;
	}

	.intro,
	.intro-block p,
	.section-heading p,
	.interest-card p,
	.project-card p {
		color: #cbd5e1;
		font-size: 1.08rem;
		line-height: 1.75;
	}

	.intro {
		max-width: 48rem;
		font-size: clamp(1.1rem, 2vw, 1.35rem);
	}

	.hero-actions,
	.social-list {
		display: flex;
		flex-wrap: wrap;
		gap: 0.75rem;
		align-items: center;
	}

	.hero-actions {
		margin-top: 1.8rem;
	}

	.button,
	.social-list a {
		display: inline-flex;
		align-items: center;
		justify-content: center;
		min-height: 3rem;
		border: 1px solid rgb(255 255 255 / 22%);
		border-radius: 8px;
		padding: 0 1.1rem;
		font-weight: 850;
		text-decoration: none;
		transition: transform 160ms ease, border-color 160ms ease, background 160ms ease;
	}

	.button:hover,
	.social-list a:hover {
		transform: translateY(-2px);
		text-decoration: none;
	}

	.primary,
	.social-list a:first-child {
		background: #f4b35e;
		border-color: #f4b35e;
		color: #111827;
	}

	.secondary,
	.social-list a:last-child {
		background: rgb(255 255 255 / 10%);
		color: #ffffff;
	}

	.ghost {
		background: transparent;
		color: #ffffff;
	}

	.hero-strip {
		display: flex;
		flex-wrap: wrap;
		gap: 0.65rem;
		border-top: 1px solid rgb(255 255 255 / 16%);
		padding-top: 1rem;
		color: #e5e7eb;
		font-size: 0.82rem;
		font-weight: 800;
		letter-spacing: 0.08em;
		text-transform: uppercase;
	}

	.hero-strip span {
		border: 1px solid rgb(255 255 255 / 18%);
		border-radius: 999px;
		padding: 0.45rem 0.75rem;
		background: rgb(255 255 255 / 7%);
	}

	.section-block {
		padding: clamp(4rem, 8vw, 7rem) 0;
		border-top: 1px solid rgb(255 255 255 / 9%);
	}

	.intro-block {
		display: grid;
		gap: 2rem;
		align-items: start;
	}

	.section-heading {
		max-width: 42rem;
	}

	.section-heading.wide {
		max-width: 64rem;
	}

	.interest-grid {
		display: grid;
		grid-template-columns: 1fr;
		gap: 1rem;
	}

	.interest-card,
	.project-card,
	.socials {
		border: 1px solid rgb(255 255 255 / 12%);
		border-radius: 8px;
		background: rgb(255 255 255 / 5%);
		box-shadow: 0 30px 90px rgb(0 0 0 / 26%);
	}

	.interest-card {
		display: grid;
		overflow: hidden;
	}

	.interest-card img {
		width: 100%;
		height: 18rem;
		object-fit: cover;
	}

	.interest-card div {
		padding: 1.25rem;
	}

	.interest-card span {
		display: inline-flex;
		margin-bottom: 1rem;
		color: #67e8f9;
		font-weight: 900;
		letter-spacing: 0.1em;
	}

	.socials {
		display: grid;
		gap: 1.25rem;
		align-items: center;
		padding: clamp(1.25rem, 4vw, 2rem);
	}

	.project-card {
		display: grid;
		overflow: hidden;
	}

	.project-media {
		position: relative;
		min-height: 19rem;
	}

	.project-media img {
		position: absolute;
		inset: 0;
		width: 100%;
		height: 100%;
		object-fit: cover;
	}

	.project-media::after {
		content: '';
		position: absolute;
		inset: 0;
		background: linear-gradient(180deg, rgb(9 11 16 / 5%), rgb(9 11 16 / 72%));
	}

	.status-tag {
		position: absolute;
		left: 1rem;
		top: 1rem;
		z-index: 1;
		display: inline-flex;
		align-items: center;
		min-height: 1.95rem;
		border: 1px solid #f4b35e;
		border-radius: 999px;
		padding: 0 0.78rem;
		background: rgb(9 11 16 / 78%);
		color: #f4b35e;
		font-size: 0.76rem;
		font-weight: 900;
		letter-spacing: 0.1em;
		text-transform: uppercase;
	}

	.project-copy {
		padding: clamp(1.35rem, 4vw, 2.5rem);
	}

	.project-copy .button {
		margin-top: 0.5rem;
	}

	@media (min-width: 760px) {
		.intro-block,
		.socials {
			grid-template-columns: minmax(0, 0.85fr) minmax(18rem, 1fr);
		}

		.interest-grid {
			grid-template-columns: repeat(3, minmax(0, 1fr));
		}

		.movie-card {
			transform: translateY(2rem);
		}

		.web-card {
			transform: translateY(4rem);
		}

		.project-card {
			grid-template-columns: minmax(22rem, 0.92fr) minmax(0, 1fr);
		}

		.project-media {
			min-height: 31rem;
		}
	}

	@media (max-width: 560px) {
		.hero {
			min-height: 680px;
		}

		.interest-card img {
			height: 14rem;
		}
	}
</style>
