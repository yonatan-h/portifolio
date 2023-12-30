<script>
    import Intro from './sections/Intro.svelte'
    import About from './sections/About.svelte';

    import One from './sections/projects/One.svelte';
    import Two from './sections/projects/Two.svelte';
    import Three from './sections/projects/Three.svelte';
    import Four from './sections/projects/Four.svelte';
	import Contact from './sections/Contact.svelte';

    import Cloud from './components/Cloud.svelte';
	import Five from './sections/projects/Five.svelte';

    const positions = []
    for (let i = 0; i < 15; i++){
        const x = Math.floor(Math.random()*100)
        const y = 10 + Math.floor(Math.random()*80)
        const duration = Math.floor(1000 + Math.random()*100)
        positions.push([x,y, duration])
    }

</script>

<Intro/>
<About/>

<One/>
<div class="relative overflow-hidden" >

	{#each positions as [x,y, duration] }
		<Cloud {x} {y} {duration}/>
	{/each}

    <Two/>
    <Three/>
    <Four/>
    <Five/>
</div>

<Contact/>