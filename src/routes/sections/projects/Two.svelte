
<script>
	import Project from '../../components/Project.svelte';
	import spark from '$lib/assets/spark.png'
</script>

<div class="sec-container night-to-day">
	<section>
		<Project
			title={'#2 Spark'}
			id={'spark'}
			link={'https://github.com/primequantuM4/Spark-Dating_Project-'}
			imageSrc={spark}
			sentences={[
				`Spark is a school project made by a team of 10 students. It is a dating website made for Ethiopians. Users select their partner preferences, match, and text chat.`,
				'I was fully responsible for the implementing the backend having user authentication, chatting, and matching.'
			]}
			technologies={[
				'Express.js', 'MongoDB', 'WebSockets', 'Cookies'
			]}
		/>
	</section>
</div>

<style>
	.night-to-day{
		background: linear-gradient(var(--night-blue), var(--morning-sky));
	}
</style>