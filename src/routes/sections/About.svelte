<script>
	import Star from '../components/Star.svelte';
	import SkillItem from '../components/SkillItem.svelte';

	import js from '$lib/assets/logos/js.svg';
	import html from '$lib/assets/logos/html.svg';
	import css from '$lib/assets/logos/css.svg';
	import express from '$lib/assets/logos/express.svg';
	import mongo from '$lib/assets/logos/mongo.svg';
	import figma from '$lib/assets/logos/figma.svg';
	import python from '$lib/assets/logos/python.svg';
	import react from '$lib/assets/logos/react.svg';
	import chrome from '$lib/assets/logos/chrome.svg';
	import ts from '$lib/assets/logos/ts.svg';
	import tailwind from '$lib/assets/logos/tailwind.svg';
	import mysql from '$lib/assets/logos/mysql.svg';
	import flutter from '$lib/assets/logos/flutter.svg';
	import svelte from '$lib/assets/logos/svelte.svg';
	import vue from '$lib/assets/logos/vue.svg';
	import nuxt from '$lib/assets/logos/nuxt.svg';


	const positions = [];
	for (let i = 0; i < 50; i++) {
		const x = Math.floor(Math.random() * 100);
		const y = Math.floor(Math.random() * 100);
		positions.push([x, y]);
	}

	const advancedSkills = [
		{
			title: 'JavaScript',
			imageSrc: js
		},
		{
			title: 'HTML',
			imageSrc: html
		},
		{
			title: 'CSS',
			imageSrc: css
		},
		{
			title: 'Express.js',
			imageSrc: express
		},
		{
			title: 'MongoDB',
			imageSrc: mongo
		},
		{
			title: 'Figma',
			imageSrc: figma
		},
		{
			title: 'Python',
			imageSrc: python
		},
	]

	const intermediateSkills = [
		{
			title: 'React.js',
			imageSrc: react
		},
		{
			title: 'Chrome Extensions',
			imageSrc: chrome
		},
		{
			title: 'TypeScript',
			imageSrc: ts
		},
		{
			title: 'Tailwind CSS',
			imageSrc: tailwind
		},
		{
			title: 'MySQL',
			imageSrc: mysql
		},
		{
			title: 'Flutter',
			imageSrc: flutter
		}
	]

	const beginnerSkills = [
		{
			title: 'SvelteKit',
			imageSrc: svelte
		},
		{
			title: 'Vue-3',
			imageSrc: vue
		},
		{
			title: 'Nuxt-3',
			imageSrc: nuxt
		}
	]
</script>

<div class="space-to-earth sec-container relative">
	{#each positions as [x, y]}
		<Star {x} {y} fuzzy={Math.random() < 0.25} wait={true} />
	{/each}

	<section class="flex flex-col md:flex-row md:justify-between gap-10 pb-40 pt-40">
		<div class="max-w-md backdrop-blur">
			<h2 class="text-4xl oswald">About Me</h2>
			<ul class="mt-5">
				<li>
					I'm a 4th year software engineering student in Addis Ababa University, Ethiopia.
					Graduating in 2025.
				</li>
				<li>The web development world is my favorite. I want to excel at it.</li>
				<li>
					As a member of A2SV(Africa to Silicon Valley), I have learned Data Structures and
					Algorithms. I did 600+ questions in LeetCode and Codeforces.
				</li>
			</ul>
		</div>

		<div class="max-w-md backdrop-blur ">
			<h2 class="text-4xl oswald ">Skills</h2>

			<div class="mt-5 flex flex-col md:flex-row justify-between gap-10">
				<div class="flex-1">
					<h3 class="oswald text-2xl pb-2">Advanced</h3>
					<ul>
						{#each advancedSkills as skill}
							<SkillItem title={skill.title} imageSrc={skill.imageSrc}/>
						{/each}
					</ul>
				</div>
				<div class="flex-1">
					<h3 class="oswald text-2xl pb-2">Intermediate</h3>
					{#each intermediateSkills as skill}
							<SkillItem title={skill.title} imageSrc={skill.imageSrc}/>
						{/each}
				</div>
				<div class="flex-1">
					<h3 class="oswald text-2xl pb-2">Beginner</h3>
					{#each beginnerSkills as skill}
							<SkillItem title={skill.title} imageSrc={skill.imageSrc}/>
						{/each}
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
