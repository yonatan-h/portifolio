<script>
	import Project from '../../components/Project.svelte';
	import xrayremake from '$lib/assets/xrayremake.png';
</script>

<div class="sec-container morning-sky">
	<section>
		<Project
			title={'#4 X-Ray Remake'}
			link={'https://github.com/yonatan-h/x-ray-remake'}
			id={'xrayremake'}
			imageSrc={xrayremake}
			sentences={[
				`This school project was a redesigned version of an 
				<a href="http://www.pnwx.com/" class="underline">user unfriendly medical equipments website</a>.`,
				`Using Bootstrap, I stylized our website with the team.`,
				`Refactored the website to use a template engine to avoid redundant pages`
			]}
			technologies={['Figma', 'Agile Software Development']}
		/>
	</section>
</div>

<!-- <a class="underline" href="http://www.pnwx.com/">medical equipments website <a/>  -->
