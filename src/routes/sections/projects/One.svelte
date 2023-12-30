<script>
	import Project from '../../components/Project.svelte';
	import Star from '../../components/Star.svelte';
	import infoblender from '$lib/assets/infoblender.png'
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
			title={'#1 Infoblender'}
			link={'https://github.com/NathanZlion/Info_Blend'}
			id={'infoblender'}
			imageSrc={infoblender}
			sentences={[
				`It is a web app that gives you articles from 150,000 news sources. 
				It let's you compare and contrast articles that discuss the same news event.`,
				`I integrated the News API SDK it into our Express.js backend after researching thier 21 page documentation.`,
				`I also implemented 5 pages using a minimalistic design style to make the website navigable.`,
			]}
			technologies={['React.js', 'Tailwind CSS', 'Framer Motion', 'Express.js', 'TypeScript']}
		/>

	</section>
</div>
