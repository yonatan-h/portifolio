<script>
	import Project from '../../components/Project.svelte';
	import Cloud from '../../components/Cloud.svelte';
	import fitquest from '$lib/assets/fitquest.png'

	const positions = []
	for (let i = 0; i < 10; i++){
		const x = Math.floor(Math.random()*120)
		const y = Math.floor(-50 + Math.random()*200)
		const duration = 800 +  Math.random() * 100
		positions.push([x,y, duration])
	}

</script>

<div class="sec-container morning-sky relative oveflow-x-hidden	">
	{#each positions as [x,y, duration] }
		<Cloud {x} {y} {duration}/>
	{/each}
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
