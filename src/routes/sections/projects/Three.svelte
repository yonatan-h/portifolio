<script>
	import Project from '../../components/Project.svelte';
	import Cloud from '../../components/Cloud.svelte';
	import fitquest from '$lib/assets/fitquest.png'


</script>

<div class="sec-container morning-sky">
	<section>
		<Project
			title={'#3 Fitquest'}
			id={'fitquest'}
			imageSrc={fitquest}
			sentences={[
				`10 of us in Upsurge, a freelancing start-up team,
                 decided to do Fitquest as our first project.
                  It is a fitness app that schedules workout plans,
                   tracks nutrition, and finds nearby gyms`,
				`I collaboratively created 60+ questionare questions to gather product requirements.
                Using the feedback of the team, I designed 30+ pages of the app in Figma.`
			]}
			technologies={['Figma', 'Agile Software Development']}
		/>
	</section>
</div>
