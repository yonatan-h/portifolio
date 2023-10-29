<script>
	import Project from '../../components/Project.svelte';
	import Star from '../../components/Star.svelte';
	import mirkusve from '$lib/assets/mirkusve.png'
	const positions = [];

	for (let i = 0; i < 20; i++) {
		const x = Math.floor(Math.random() * 100);
		const y = Math.floor(Math.random() * 80);
		positions.push([x, y]);
	}
</script>

<div class="sec-container night-blue relative">
	{#each positions as [x, y]}
		<Star {x} {y} fuzzy={true} wait={true} />
	{/each}
	<section>
		<Project
			title={'#1 Mirkusve'}
			id={'mirkusve'}
			link={'https://github.com/yonatan-h/mirkusve2'}
			imageSrc={mirkusve}
			sentences={[
				`After answering a LeetCode quesion, I had to upload the answer's code to GitHub and then attach it in A2SV's Google Sheets. It was tiresome.`,
				'Mirkusve is a Chrome Extension that automates this process for A2SV students.'
			]}
			technologies={['React.js', 'Google Apps Script', 'Github Apps', 'Chrome Extensions']}
		/>
	</section>
</div>
