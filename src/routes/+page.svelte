<script>
	import '@fontsource/martian-mono';
	import '@fontsource/martian-mono/700.css';
	import '@fontsource/big-shoulders-display/700.css';
	import '@fontsource/big-shoulders-display/800.css';
	import { tick } from 'svelte';

	const entries = [
		{
			id: 'founderblocks',
			toc: 'FULLSTACK ENGINEER · FOUNDERBLOCKS',
			pg: '2019-NOW',
			title: 'Fullstack Engineer',
			org: 'FounderBlocks',
			period: 'November 2019 to Current',
			stack: 'ANGULAR / REACT / FLUTTER / DJANGO / NGRX / RXJS / PLAYWRIGHT',
			bullets: [
				'Delivered and maintained complex UI features using Angular, React and Flutter, integrating with Django-based APIs and custom component libraries.',
				'Implemented scalable state management with NgRx, RxJS and context-based patterns to support role-specific views, dynamic forms and data-heavy modules.',
				'Led frontend refactors into modular, testable components, improving performance and developer velocity across large-scale web and mobile apps.',
				'Contributed to CI/CD pipelines and Playwright-based test suites, and collaborated on performance monitoring and accessibility improvements in production.'
			]
		},
		{
			id: 'indianexpress',
			toc: 'DATA DEVELOPER · INDIAN EXPRESS',
			pg: '2018-19',
			title: 'Data Developer',
			org: 'The Indian Express',
			period: 'July 2018 to October 2019',
			stack: 'D3.JS / JAVASCRIPT / DATA VISUALISATION',
			bullets: [
				'Built interactive, mobile-friendly data visualisations for high-traffic election coverage using D3.js.',
				'Worked closely with editors and backend teams to deliver real-time vote updates, map visualisations and performance-optimised visual storytelling for mobile users.'
			]
		},
		{
			id: 'gsoc',
			toc: 'GOOGLE SUMMER OF CODE · COALA',
			pg: '2017',
			title: 'Google Summer of Code 2017',
			org: 'coala',
			period: 'May 2017 to August 2017',
			stack: 'PYTHON / DJANGO / JAVASCRIPT / DOCKER',
			bullets: [
				"Contributed to coala's open-source ecosystem by developing the coala Online module for web-based code analysis.",
				'Built with Python, Django, JavaScript and Docker.'
			]
		},
		{
			id: 'education',
			toc: 'B.TECH CSE · GGSIP UNIVERSITY',
			pg: '2014-18',
			title: 'B.Tech, Computer Science & Engineering',
			org: 'GGSIP University, Delhi, India',
			period: 'September 2014 to May 2018',
			stack: 'COMPUTER SCIENCE / ENGINEERING',
			bullets: [
				'Four-year undergraduate degree in Computer Science & Engineering from Guru Gobind Singh Indraprastha University, Delhi.'
			]
		},
		{
			id: 'cert',
			toc: 'INFORMATION VISUALISATION · COURSERA',
			pg: 'CERT',
			title: 'Information Visualisation Specialisation',
			org: 'Coursera',
			period: 'Certification',
			stack: 'DATA VISUALISATION / PERCEPTION / DASHBOARDS',
			bullets: [
				'Completed the Information Visualisation Specialisation on Coursera, covering visual perception, visualisation design and applied dashboard construction.'
			]
		}
	];

	const skills = [
		'HTML5 / CSS',
		'TYPESCRIPT',
		'REACT',
		'ANGULAR',
		'SVELTE',
		'NGRX / RXJS',
		'DJANGO',
		'FASTAPI',
		'D3.JS',
		'PLAYWRIGHT'
	];

	let open = $state(null);
	let lastTrigger = null;

	async function openPage(id, ev) {
		lastTrigger = ev.currentTarget;
		open = id;
		await tick();
		document.querySelector('.article.open .close')?.focus();
	}
	async function close() {
		open = null;
		await tick();
		lastTrigger?.focus();
	}

	const ld = JSON.stringify({
		'@context': 'https://schema.org',
		'@graph': [
			{
				'@type': 'WebSite',
				'@id': 'https://hemang.dev/#website',
				url: 'https://hemang.dev/',
				name: 'hemang.dev',
				publisher: { '@id': 'https://hemang.dev/#person' }
			},
			{
				'@type': 'ProfilePage',
				'@id': 'https://hemang.dev/#page',
				url: 'https://hemang.dev/',
				name: 'Hemang Kumar | Software Engineer',
				isPartOf: { '@id': 'https://hemang.dev/#website' },
				about: { '@id': 'https://hemang.dev/#person' },
				mainEntity: { '@id': 'https://hemang.dev/#person' },
				dateModified: '2026-07-05'
			},
			{
				'@type': 'Person',
				'@id': 'https://hemang.dev/#person',
				name: 'Hemang Kumar',
				alternateName: 'hemangsk',
				url: 'https://hemang.dev/',
				image: 'https://hemang.dev/og.png',
				jobTitle: 'Software Engineer',
				worksFor: { '@type': 'Organization', name: 'FounderBlocks' },
				alumniOf: { '@type': 'CollegeOrUniversity', name: 'GGSIP University, Delhi' },
				address: { '@type': 'PostalAddress', addressLocality: 'New Delhi', addressCountry: 'IN' },
				sameAs: ['https://github.com/hemangsk'],
				knowsAbout: [
					'HTML5', 'CSS', 'TypeScript', 'React', 'Angular', 'Svelte', 'Django',
					'FastAPI', 'NgRx', 'RxJS', 'D3.js', 'Playwright', 'Flutter'
				],
				hasCredential: {
					'@type': 'EducationalOccupationalCredential',
					name: 'Information Visualisation Specialisation',
					credentialCategory: 'certificate',
					recognizedBy: { '@type': 'Organization', name: 'Coursera' }
				}
			}
		]
	}).replace(/</g, '\\u003c');
</script>

<svelte:head>
	<title>Hemang Kumar | Software Engineer · Angular, React, TypeScript</title>
	<meta
		name="description"
		content="Hemang Kumar is a software engineer building maintainable Angular, React and TypeScript UIs for high-trust web and mobile products at FounderBlocks."
	/>
	<meta name="author" content="Hemang Kumar" />
	<meta name="robots" content="index, follow" />
	<link rel="canonical" href="https://hemang.dev/" />
	<meta property="og:type" content="profile" />
	<meta property="og:locale" content="en_US" />
	<meta property="profile:first_name" content="Hemang" />
	<meta property="profile:last_name" content="Kumar" />
	<meta property="profile:username" content="hemangsk" />
	<meta property="og:url" content="https://hemang.dev/" />
	<meta property="og:site_name" content="hemang.dev" />
	<meta property="og:title" content="Hemang Kumar | Software Engineer" />
	<meta
		property="og:description"
		content="Software engineer building maintainable Angular, React and TypeScript UIs for high-trust web and mobile products. Fullstack engineer at FounderBlocks."
	/>
	<meta property="og:image" content="https://hemang.dev/og.png" />
	<meta property="og:image:width" content="1200" />
	<meta property="og:image:height" content="630" />
	<meta property="og:image:alt" content="Hemang Kumar, software engineer. Monochrome cover of hemang.dev" />
	<meta name="twitter:card" content="summary_large_image" />
	<meta name="twitter:title" content="Hemang Kumar | Software Engineer" />
	<meta
		name="twitter:description"
		content="Software engineer building maintainable Angular, React and TypeScript UIs for high-trust web and mobile products."
	/>
	<meta name="twitter:image" content="https://hemang.dev/og.png" />
	<meta name="twitter:image:alt" content="Hemang Kumar, software engineer. Monochrome cover of hemang.dev" />
	{@html `<script type="application/ld+json">${ld}<\/script>`}
</svelte:head>

<svelte:window onkeydown={(e) => e.key === 'Escape' && open && close()} />

<div class="page">
	<span class="reg tl" aria-hidden="true">+</span>
	<span class="reg tr" aria-hidden="true">+</span>
	<span class="reg bl" aria-hidden="true">+</span>
	<span class="reg br" aria-hidden="true">+</span>

	<header class="topbar" inert={open !== null}>
		<span class="brand">HEMANG.DEV</span>
		<span class="issue">ISSUE 08 · JUL 2026</span>
		<span class="coords">28.6139°N 77.2090°E · NEW DELHI</span>
	</header>

	<main class="spread" inert={open !== null}>
		<section class="profile" aria-labelledby="profile-h">
			<h2 class="label" id="profile-h">PROFILE</h2>
			<p class="kicker">SOFTWARE ENGINEER</p>
			<h1 class="name">HEMANG KUMAR</h1>
			<p class="dek">Maintainable interfaces for high-trust software.</p>
			<p class="bio">
				Building UIs across Angular, React and Django stacks. Apps shipped for high-trust
				domains such as health, parenting and cognitive wellbeing, plus CRM systems for
				safety compliance and audits. Focused on thoughtful, well-crafted software that
				improves everyday life.
			</p>
			<p class="links">
				<a href="https://github.com/hemangsk" rel="me">GITHUB <span aria-hidden="true">↗</span></a>
			</p>
			<div class="stack">
				<h3 class="label">STACK</h3>
				<!-- svelte-ignore a11y_no_redundant_roles -->
				<ul class="chips" role="list">
					{#each skills as s}
						<li>{s}</li>
					{/each}
				</ul>
			</div>
		</section>

		<section class="index" aria-labelledby="index-h">
			<h2 class="label" id="index-h">INDEX / 2014-2026</h2>
			<!-- svelte-ignore a11y_no_redundant_roles -->
			<ol class="toc" role="list">
				{#each entries as e, i (e.id)}
					<li style="--i:{i}">
						<button class="row" onclick={(ev) => openPage(e.id, ev)}>
							<span class="row-main">
								<span class="num">0{i + 1}</span>
								<span class="row-title">{e.toc}</span>
								<span class="dots" aria-hidden="true"></span>
								<span class="pg">{e.pg}</span>
							</span>
							<span class="row-sub">{e.stack}</span>
						</button>
					</li>
				{/each}
			</ol>
		</section>
	</main>

	<footer class="foot" inert={open !== null}>
		<span>© 2026 HEMANG KUMAR</span>
		<span class="barcode" aria-hidden="true"></span>
	</footer>

	{#each entries as e, i (e.id)}
		<article
			class="article"
			class:open={open === e.id}
			role="dialog"
			aria-modal="true"
			aria-labelledby="a-{e.id}"
		>
			<div class="article-inner">
				<header class="article-head">
					<span>HEMANG.DEV · INDEX N°0{i + 1}</span>
					<span>ESC TO CLOSE</span>
				</header>
				<h3 id="a-{e.id}">{e.title}</h3>
				<p class="article-meta">{e.org} · {e.period}</p>
				<!-- svelte-ignore a11y_no_noninteractive_tabindex -->
				<div class="article-scroll" tabindex="0" role="region" aria-labelledby="a-{e.id}">
					<!-- svelte-ignore a11y_no_redundant_roles -->
					<ul class="article-bullets" role="list">
						{#each e.bullets as b}
							<li>{b}</li>
						{/each}
					</ul>
				</div>
				<p class="article-stack">{e.stack}</p>
				<button class="close" onclick={close}><span aria-hidden="true">←</span> BACK</button>
			</div>
		</article>
	{/each}

	<div class="grain" aria-hidden="true"></div>
</div>

<style>
	:global(html, body) {
		height: 100%;
		margin: 0;
		overflow: hidden;
		background: #0f0f0e;
	}
	:global(::selection) {
		background: #e8e8e2;
		color: #0f0f0e;
	}
	@media (prefers-color-scheme: light) {
		:global(html, body) {
			background: #f0efe9;
		}
		:global(::selection) {
			background: #0f0f0e;
			color: #f0efe9;
		}
	}

	.page {
		--bg: #0f0f0e;
		--ink: #d9d9d3;
		--bright: #f4f4ee;
		--dim: #84847d;
		--rule: #2e2e2a;
		--scanline: rgba(255, 255, 255, 0.016);
		--pad: clamp(0.8rem, 2.4vmin, 2rem);
		box-sizing: border-box;
		height: 100vh;
		height: 100dvh;
		display: grid;
		grid-template-rows: auto minmax(0, 1fr) auto;
		padding: var(--pad);
		background: var(--bg);
		color: var(--ink);
		font-family: 'Martian Mono', 'Courier New', monospace;
		position: relative;
		overflow: hidden;
	}
	@media (prefers-color-scheme: light) {
		.page {
			--bg: #f0efe9;
			--ink: #2b2b26;
			--bright: #111110;
			--dim: #63635c;
			--rule: #d8d6cc;
			--scanline: rgba(0, 0, 0, 0.02);
		}
	}
	.page :global(*),
	.page :global(*::before),
	.page :global(*::after) {
		box-sizing: border-box;
	}

	.reg {
		position: absolute;
		color: var(--dim);
		font-size: 0.7rem;
		line-height: 1;
		padding: 0.35rem;
		user-select: none;
	}
	.tl { top: 0; left: 0; }
	.tr { top: 0; right: 0; }
	.bl { bottom: 0; left: 0; }
	.br { bottom: 0; right: 0; }

	/* ---------- topbar ---------- */
	.topbar {
		display: flex;
		justify-content: space-between;
		align-items: baseline;
		gap: 1rem;
		padding-bottom: clamp(0.4rem, 1.2vmin, 0.8rem);
		border-bottom: 3px double var(--rule);
		font-size: clamp(0.55rem, 1.4vmin, 0.72rem);
		letter-spacing: 0.18em;
		color: var(--dim);
		animation: fade 0.6s both;
	}
	.brand {
		color: var(--bright);
		font-weight: 700;
	}

	/* ---------- spread ---------- */
	.spread {
		display: grid;
		grid-template-columns: minmax(0, 5fr) minmax(0, 7fr);
		min-height: 0;
	}
	section {
		min-height: 0;
		overflow: hidden;
		display: flex;
		flex-direction: column;
		gap: clamp(0.5rem, 1.6vmin, 1rem);
		padding: clamp(0.7rem, 2.2vmin, 1.6rem) 0;
	}
	.profile {
		padding-right: clamp(0.8rem, 2.5vmin, 2rem);
		border-right: 1px solid var(--rule);
		animation: fade 0.6s 0.15s both;
	}
	.index {
		padding-left: clamp(0.8rem, 2.5vmin, 2rem);
		animation: fade 0.6s 0.3s both;
	}

	.label {
		margin: 0;
		font-size: clamp(0.5rem, 1.2vmin, 0.62rem);
		font-weight: 400;
		letter-spacing: 0.3em;
		color: var(--dim);
		border-bottom: 1px solid var(--rule);
		padding-bottom: 0.6em;
	}
	.kicker {
		margin: 0;
		font-size: clamp(0.55rem, 1.5vmin, 0.75rem);
		letter-spacing: 0.4em;
		color: var(--dim);
	}
	.name {
		margin: 0;
		font-family: 'Big Shoulders Display', 'Martian Mono', sans-serif;
		font-weight: 800;
		font-size: clamp(2rem, 7vmin, 3.8rem);
		line-height: 0.95;
		letter-spacing: 0.02em;
		color: var(--bright);
		animation: rise 0.6s 0.25s both;
	}
	.dek {
		margin: 0;
		font-size: clamp(0.62rem, 1.7vmin, 0.85rem);
		font-weight: 700;
		color: var(--ink);
		letter-spacing: 0.04em;
	}
	.bio {
		margin: 0;
		font-size: clamp(0.6rem, 1.6vmin, 0.78rem);
		line-height: 1.75;
		color: var(--dim);
		max-width: 46ch;
	}
	.links {
		margin: 0;
	}
	.links a {
		color: var(--bright);
		font-weight: 700;
		font-size: clamp(0.58rem, 1.5vmin, 0.72rem);
		letter-spacing: 0.15em;
		text-decoration: none;
		border-bottom: 1px solid var(--dim);
		padding-bottom: 0.2em;
	}
	.links a:hover,
	.links a:focus-visible {
		background: var(--bright);
		color: var(--bg);
		border-color: var(--bright);
	}

	.stack {
		margin-top: auto;
		display: grid;
		gap: clamp(0.4rem, 1.2vmin, 0.7rem);
	}
	.chips {
		list-style: none;
		margin: 0;
		padding: 0;
		display: flex;
		flex-wrap: wrap;
		gap: clamp(0.25rem, 0.8vmin, 0.45rem);
	}
	.chips li {
		border: 1px solid var(--rule);
		padding: 0.3em 0.6em;
		font-size: clamp(0.5rem, 1.3vmin, 0.62rem);
		letter-spacing: 0.14em;
		color: var(--ink);
	}
	.chips li:hover {
		background: var(--ink);
		color: var(--bg);
		border-color: var(--ink);
	}

	/* ---------- index ---------- */
	.toc {
		list-style: none;
		margin: 0;
		padding: 0;
		flex: 1;
		display: grid;
		grid-template-columns: minmax(0, 1fr);
		align-content: space-evenly;
		gap: clamp(0.2rem, 0.8vmin, 0.5rem);
	}
	.toc li {
		min-width: 0;
		animation: rise 0.5s calc(0.4s + var(--i) * 0.08s) both;
		border-bottom: 1px solid var(--rule);
	}
	.toc li:last-child {
		border-bottom: none;
	}
	.row {
		all: unset;
		box-sizing: border-box;
		display: grid;
		grid-template-columns: minmax(0, 1fr);
		gap: 0.45em;
		width: 100%;
		padding: clamp(0.35em, 1.2vmin, 0.7em) 0.4em;
		font-family: inherit;
		font-size: clamp(0.6rem, 1.7vmin, 0.85rem);
		letter-spacing: 0.05em;
		cursor: pointer;
	}
	.row:hover,
	.row:focus-visible {
		background: var(--ink);
		color: var(--bg);
	}
	.row:focus-visible {
		outline: 1px dashed var(--dim);
		outline-offset: 2px;
	}
	.row-main {
		display: flex;
		align-items: baseline;
		gap: 0.8em;
		min-width: 0;
	}
	.row-sub {
		min-width: 0;
	}
	.num {
		color: var(--dim);
		font-size: 0.8em;
	}
	.row:hover .num,
	.row:focus-visible .num {
		color: var(--bg);
	}
	.row-title {
		font-weight: 700;
		color: var(--bright);
		white-space: nowrap;
		overflow: hidden;
		text-overflow: ellipsis;
		min-width: 0;
		flex-shrink: 1;
	}
	.row:hover .row-title,
	.row:focus-visible .row-title {
		color: var(--bg);
	}
	.dots {
		flex: 1;
		min-width: 1.5em;
		height: 0.5em;
		background-image: radial-gradient(circle, var(--dim) 0.8px, transparent 1.2px);
		background-size: 7px 7px;
		background-position: left center;
		background-repeat: repeat-x;
	}
	.row:hover .dots,
	.row:focus-visible .dots {
		background-image: radial-gradient(circle, var(--bg) 0.8px, transparent 1.2px);
	}
	.pg {
		color: var(--dim);
		font-size: 0.85em;
		white-space: nowrap;
	}
	.row:hover .pg,
	.row:focus-visible .pg {
		color: var(--bg);
	}
	.row-sub {
		font-size: 0.68em;
		letter-spacing: 0.2em;
		color: var(--dim);
		padding-left: 2.6em;
	}
	.row:hover .row-sub,
	.row:focus-visible .row-sub {
		color: var(--bg);
		opacity: 0.75;
	}

	/* ---------- footer ---------- */
	.foot {
		display: flex;
		justify-content: space-between;
		align-items: center;
		gap: 1rem;
		border-top: 1px solid var(--rule);
		padding-top: clamp(0.4rem, 1.2vmin, 0.8rem);
		font-size: clamp(0.52rem, 1.3vmin, 0.68rem);
		letter-spacing: 0.18em;
		color: var(--dim);
		animation: fade 0.6s 0.5s both;
	}
	.barcode {
		width: clamp(4rem, 9vw, 7.5rem);
		height: clamp(0.7rem, 1.8vmin, 1.1rem);
		color: var(--dim);
		background:
			repeating-linear-gradient(90deg, currentColor 0 2px, transparent 2px 5px, currentColor 5px 6px, transparent 6px 10px),
			repeating-linear-gradient(90deg, currentColor 0 1px, transparent 1px 7px);
		opacity: 0.7;
	}

	/* ---------- article overlay ---------- */
	.article {
		display: none;
		position: absolute;
		inset: 0;
		z-index: 10;
		background: var(--bg);
		padding: var(--pad);
	}
	.article.open {
		display: grid;
		animation: page-in 0.3s both;
	}
	.article-inner {
		border: 1px solid var(--rule);
		padding: clamp(1rem, 3.5vmin, 2.4rem);
		display: flex;
		flex-direction: column;
		gap: clamp(0.6rem, 2vmin, 1.2rem);
		min-height: 0;
		overflow: hidden;
	}
	.article-head {
		display: flex;
		justify-content: space-between;
		gap: 1rem;
		font-size: clamp(0.52rem, 1.4vmin, 0.68rem);
		letter-spacing: 0.25em;
		color: var(--dim);
		border-bottom: 1px solid var(--rule);
		padding-bottom: 0.8em;
	}
	.article h3 {
		margin: 0;
		font-family: 'Big Shoulders Display', sans-serif;
		font-weight: 800;
		font-size: clamp(1.6rem, 6vmin, 3.4rem);
		line-height: 0.95;
		text-transform: uppercase;
		color: var(--bright);
	}
	.article-meta {
		margin: 0;
		font-weight: 700;
		font-size: clamp(0.6rem, 1.7vmin, 0.8rem);
		letter-spacing: 0.1em;
	}
	.article-scroll {
		overflow-y: auto;
		min-height: 0;
	}
	.article-scroll:focus-visible {
		outline: 1px dashed var(--dim);
		outline-offset: 4px;
	}
	.article-bullets {
		margin: 0;
		padding: 0;
		list-style: none;
		display: grid;
		gap: clamp(0.5rem, 1.6vmin, 1rem);
		font-size: clamp(0.62rem, 1.8vmin, 0.82rem);
		line-height: 1.8;
		color: var(--ink);
		max-width: 72ch;
	}
	.article-bullets li {
		padding-left: 1.4em;
		position: relative;
	}
	.article-bullets li::before {
		content: '▪';
		position: absolute;
		left: 0;
		color: var(--dim);
	}
	.article-stack {
		margin: 0;
		font-size: clamp(0.5rem, 1.3vmin, 0.62rem);
		letter-spacing: 0.25em;
		color: var(--dim);
	}
	.close {
		all: unset;
		box-sizing: border-box;
		margin-top: auto;
		align-self: flex-start;
		border: 1px solid var(--dim);
		padding: 0.5em 1em;
		font-family: inherit;
		font-weight: 700;
		font-size: clamp(0.6rem, 1.6vmin, 0.75rem);
		letter-spacing: 0.15em;
		color: var(--bright);
		cursor: pointer;
	}
	.close:hover,
	.close:focus-visible {
		background: var(--bright);
		color: var(--bg);
		border-color: var(--bright);
	}

	/* ---------- texture ---------- */
	.grain {
		position: absolute;
		inset: 0;
		z-index: 50;
		pointer-events: none;
		opacity: 0.5;
		background-image:
			repeating-linear-gradient(0deg, var(--scanline) 0 1px, transparent 1px 3px),
			url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="180" height="180"><filter id="n"><feTurbulence type="fractalNoise" baseFrequency="0.85" numOctaves="2"/><feColorMatrix type="matrix" values="0 0 0 0 0.9 0 0 0 0 0.9 0 0 0 0 0.9 0 0 0 0.05 0"/></filter><rect width="180" height="180" filter="url(%23n)"/></svg>');
	}
	@media (prefers-color-scheme: light) {
		.grain {
			background-image:
				repeating-linear-gradient(0deg, var(--scanline) 0 1px, transparent 1px 3px),
				url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="180" height="180"><filter id="n"><feTurbulence type="fractalNoise" baseFrequency="0.85" numOctaves="2"/><feColorMatrix type="matrix" values="0 0 0 0 0.1 0 0 0 0 0.1 0 0 0 0 0.1 0 0 0 0.05 0"/></filter><rect width="180" height="180" filter="url(%23n)"/></svg>');
		}
	}

	/* ---------- animation ---------- */
	@keyframes fade {
		from { opacity: 0; }
		to { opacity: 1; }
	}
	@keyframes rise {
		from { opacity: 0; transform: translateY(10px); }
		to { opacity: 1; transform: none; }
	}
	@keyframes page-in {
		from { transform: translateY(2.5%); opacity: 0; }
		to { transform: none; opacity: 1; }
	}
	@media (prefers-reduced-motion: reduce) {
		.page :global(*) {
			animation-duration: 0.01ms !important;
			animation-delay: 0s !important;
		}
	}

	/* ---------- responsive ---------- */
	@media (max-width: 880px) {
		.spread {
			grid-template-columns: 1fr;
			grid-template-rows: auto minmax(0, 1fr);
		}
		.profile {
			border-right: none;
			border-bottom: 1px solid var(--rule);
			padding-right: 0;
			padding-bottom: clamp(0.6rem, 2vmin, 1.2rem);
		}
		.index {
			padding-left: 0;
		}
		.issue {
			display: none;
		}
		.bio {
			max-width: none;
		}
	}
	@media (max-width: 880px) and (max-height: 760px) {
		.stack {
			display: none;
		}
	}
	@media (max-width: 560px) {
		.coords {
			display: none;
		}
		.toc {
			align-content: start;
			gap: 0;
		}
		.row {
			padding: 0.8em 0.2em;
		}
		.row-sub {
			display: none;
		}
		.barcode {
			display: none;
		}
		.topbar .issue {
			display: inline;
		}
		.dots {
			display: none;
		}
		.row-main {
			flex-wrap: wrap;
			row-gap: 0.35em;
		}
		.num {
			order: 1;
		}
		.pg {
			order: 2;
			margin-left: auto;
		}
		.row-title {
			order: 3;
			flex-basis: 100%;
			white-space: normal;
			overflow: visible;
			text-overflow: clip;
			line-height: 1.5;
		}
	}
	@media (max-width: 560px) and (max-height: 640px) {
		.row {
			padding: 0.45em 0.2em;
		}
		.row-main {
			row-gap: 0.25em;
		}
		.bio {
			line-height: 1.6;
		}
	}
	@media (max-height: 480px) {
		.bio,
		.stack,
		.row-sub {
			display: none;
		}
		.name {
			font-size: clamp(1.4rem, 6vmin, 2.4rem);
		}
	}
</style>
