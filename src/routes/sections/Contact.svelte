<script>
	import ground from '$lib/assets/ground.svg';
</script>

<div id={'worktogether'} class="morning-sky pt-40 sec-container">
	<section class="flex flex-col max-w-sm items-center">
			<h2 class="text-6xl oswald mb-10">What's Next?</h2>
			<p class="text-center">
				I'm looking for an internship opportunity to gain experience in doing REAL WORLD projects
			</p>
			<p class="font-bold">Let's Work Together!</p>
	</section>
</div>
<div class="flex flex-col items-center relative morning-sky pt-40">
	<span class="absolute bottom-0 opacity-20 font-bold lg:text-[10rem] text-[4rem] oswald"
		>REAL WORLD</span
	>
	<img class="ground h-[10vh] lg:h-auto" src={ground} alt="ground" />
</div>

<style>
	.ground {
		filter: brightness(0%);
		object-fit: cover;
	}
</style>
