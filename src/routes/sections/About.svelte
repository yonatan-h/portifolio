<script>
	import Star from '../components/Star.svelte';

	const positions = [];
	for (let i = 0; i < 50; i++) {
		const x = Math.floor(Math.random() * 100);
		const y = Math.floor(Math.random() * 100);
		positions.push([x, y]);
	}
</script>

<div class="space-to-earth sec-container relative">
	{#each positions as [x, y]}
		<Star {x} {y} fuzzy={Math.random() < 0.25} wait={true} />
	{/each}

	<section class="flex flex-col lg:flex-row justify-between gap-10 pb-40 pt-40">
		<div class="max-w-sm backdrop-blur">
			<h2 class="text-4xl oswald">About Me</h2>
			<ul class="mt-5">
				<li>
					I'm a 4th year software engineering student in Addis Ababa University, Ethiopia.
					Graduating in 2025.
				</li>
				<li>The web development world is my favorite. I want to excell at it.</li>
				<li>
					As a member of A2SV(Africa to Silicon Valley), I have learned Data Strucures and
					Algorithms. I did 600+ questions in leetcode and codeforces.
				</li>
			</ul>
		</div>

		<div class="max-w-sm backdrop-blur">
			<h2 class="text-4xl oswald">Skills</h2>

			<div class="mt-5 flex flex-wrap gap-10">
				<div>
					<h3 class="oswald text-2xl">Advanced</h3>
					<ul>
						<li>JavaScript</li>
						<li>HTML</li>
						<li>CSS</li>
						<li>Express.js</li>
						<li>MongoDB</li>
						<li>Figma</li>
						<li>Python</li>
					</ul>
				</div>
				<div>
					<h3 class="oswald text-2xl">Intermediate</h3>
					<ul>
						<li>React.js</li>
						<li>Chrome Extensions</li>
						<li>Java</li>
						<li>TypeScript</li>
						<li>Google Apps Script</li>
						<li>EJS</li>
					</ul>
				</div>
				<div>
					<h3 class="oswald text-2xl">Beginner</h3>
					<ul>
						<li>Linux Bash</li>
						<li>Agile Software Development</li>
						<li>Bootstrap</li>
						<li>SvelteKit</li>
						<li>Tailwind</li>
					</ul>
				</div>
			</div>
		</div>
	</section>
</div>

<style>
	.space-to-earth {
		background: linear-gradient(var(--space-dark), var(--night-blue));
	}
</style>
