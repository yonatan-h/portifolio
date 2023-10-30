<script>
	import ground from '$lib/assets/ground.svg';
</script>

<div id={'worktogether'} class="morning-sky sec-container">
	<section class="flex flex-col items-center pt-40">
		<h2 class="text-6xl oswald">What's Next?</h2>
		<p class="mt-10 max-w-sm">
			I'm looking for an internship opportunity to gain experience in working on REAL WORLD
			projects.
		</p>
		<p class="font-bold mt-5">Let's Work Together!</p>
	</section>
</div>

<div class="flex flex-col items-center relative morning-sky pt-40 bg-white">
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
