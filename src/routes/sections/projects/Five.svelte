<script>
	import Project from '../../components/Project.svelte';
	import achaye from '$lib/assets/achaye2.png';
</script>

<div class="sec-container morning-sky">
	<section>
		<Project
			title={'#5 Achaye'}
			link={'https://github.com/hayk2377/Achaye'}
			id={'achaye'}
			imageSrc={achaye}
			sentences={[
			`Achaye is a school project made by a team of 5 students. It is simply the mobile version of our dating website, Spark.`,
			`I integrated the app with the backend. I implemented Models, Data providers, and Repositories. I also setup most of the app routing.`,
			`I wrote 26 tests for the data layer in total, eliminating type conversion errors and ensuring data integrity.`			
			]}
			technologies={['Flutter', 'BLoC', 'Flutter Test', 'Integration Test', 'Go Router']}
		/>
	</section>
</div>

