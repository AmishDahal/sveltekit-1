<svelte:head>
	<title>Amish Dahal | Structure Lab</title>
	<meta
		name="description"
		content="Structure Lab is Amish Dahal's student friendly structural mechanics project for learning AFD, SFD, BMD, and tension or compression visually."
	/>
</svelte:head>

<section class="hero" aria-labelledby="page-title">
	<div class="hero-copy">
		<p class="eyebrow">Structure Lab</p>
		<h1 id="page-title">A visual study tool for AFD, SFD, and BMD.</h1>
		<p class="intro">
			This site now focuses on one student-friendly project: a structural mechanics lab where
			basic beams and trusses become clear free body diagrams, force diagrams, and bending
			moment diagrams.
		</p>
		<div class="hero-actions" aria-label="Primary actions">
			<a class="button primary" href="/structure-lab.html">Launch Structure Lab</a>
			<a class="button secondary" href="#overview">See what it does</a>
		</div>
	</div>

	<div class="lab-preview" aria-label="Structure Lab visual preview">
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
</section>

<section class="section-block" id="overview" aria-labelledby="overview-title">
	<div class="section-heading">
		<p class="eyebrow">One project</p>
		<h2 id="overview-title">Basic diagrams without the crowded canvas.</h2>
		<p>
			Structure Lab is built for learning by seeing. The interface turns a simple model into
			reactions, axial force, shear force, bending moment, and the tensile or compressive nature
			of members, with JPG sketches available as visual references.
		</p>
	</div>
	<div class="feature-grid">
		<article><h3>Start simple</h3><p>Use basic beam and truss examples instead of building custom frames before the idea is clear.</p></article>
		<article><h3>Add a sketch</h3><p>Upload a JPG picture as a reference beside the basic example students are studying.</p></article>
		<article><h3>Focus one diagram</h3><p>Click AFD, SFD, or BMD to give that diagram its own view with the free body diagram above it.</p></article>
	</div>
</section>

<section class="section-block showcase" aria-labelledby="showcase-title">
	<div>
		<p class="eyebrow">Live tool</p>
		<h2 id="showcase-title">Open the lab and start with a template.</h2>
		<p>Use a basic example, add a JPG reference if helpful, then open AFD, SFD, or BMD as a focused study view.</p>
	</div>
	<a class="button primary" href="/structure-lab.html">Launch Structure Lab</a>
</section>

<style>
	:global(html){scroll-behavior:smooth}.hero,.section-block{width:100%}.hero{display:grid;grid-template-columns:1fr;gap:2rem;align-items:center;padding:4.5rem 0 3rem}.hero-copy{max-width:47rem}.eyebrow{margin:0 0 .75rem;color:#0e5f6f;font-size:.8rem;font-weight:800;letter-spacing:.08em;text-transform:uppercase}h1,h2,h3,p{margin-top:0}h1{max-width:56rem;margin-bottom:1rem;color:#111827;font-size:clamp(2.45rem,8vw,5.25rem);font-weight:850;line-height:.98;text-align:left}h2{margin-bottom:.75rem;color:#111827;font-size:clamp(2rem,4vw,3.25rem);font-weight:800;line-height:1.05}h3{margin-bottom:.7rem;color:#15202b;font-size:1.15rem;font-weight:800}.intro,.section-heading p,.showcase p,.feature-grid p{color:#4b5b68;font-size:1.08rem;line-height:1.65}.hero-actions{display:flex;flex-wrap:wrap;gap:.75rem;margin-top:1.6rem}.button{display:inline-flex;align-items:center;justify-content:center;min-height:2.85rem;border:2px solid transparent;border-radius:8px;padding:0 1.1rem;font-weight:800;text-decoration:none}.button:focus-visible{outline:3px solid #f2b705;outline-offset:3px}.primary{background:#0e5f6f;color:#fff}.secondary{border-color:#0e5f6f;color:#0e5f6f;background:#fff}.lab-preview{overflow:hidden;border:1px solid #cbd6de;border-radius:8px;background:#fff;box-shadow:0 24px 70px rgb(24 32 42 / 14%)}.preview-header{display:flex;align-items:center;gap:.45rem;height:2.75rem;padding:0 1rem;border-bottom:1px solid #d9e1e7;background:#eef3f5;color:#40505e;font-size:.82rem}.preview-header span{width:.65rem;height:.65rem;border-radius:50%;background:#9aa7b4}.preview-header strong{margin-left:.35rem}svg{display:block;width:100%;height:auto;background:#fbfcfd}.grid{fill:none;stroke:#e4eaf0;stroke-width:1}.member,.deflected,.load path{fill:none;stroke-linecap:round;stroke-linejoin:round}.member{stroke-width:12}.compression{stroke:#cb3b3b}.frame{stroke:#7154b8}.tension{stroke:#1f8a5b}.deflected{stroke:#111827;stroke-dasharray:10 8;stroke-width:4}.load path{stroke:#0e5f6f;stroke-width:7}.nodes circle{fill:#fff;stroke:#111827;stroke-width:4}svg text{fill:#52616f;font:700 18px system-ui}.section-block{padding:3.75rem 0;border-top:1px solid #d6dde5}.section-heading{max-width:48rem;margin-bottom:1.5rem}.feature-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(16rem,1fr));gap:1rem}.feature-grid article{min-height:13rem;border:1px solid #d6dde5;border-radius:8px;padding:1.25rem;background:#fff;box-shadow:0 14px 35px rgb(24 32 42 / 7%)}.showcase{display:grid;gap:1rem;align-items:center}.showcase div{max-width:45rem}@media(min-width:820px){.hero{grid-template-columns:minmax(0,.9fr) minmax(25rem,1.1fr);padding-top:5.25rem}.showcase{grid-template-columns:1fr auto}}@media(max-width:560px){.hero{padding-top:2.5rem}h1{font-size:2.55rem}}
</style>
