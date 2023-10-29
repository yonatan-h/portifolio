<script>
	import ground from '$lib/assets/ground.svg';
</script>

<div id={'worktogether'} class="morning-sky pt-40">

	<section class="flex justify-center">
		<div class="max-w-sm">
			<h2 class="text-6xl oswald text-center">What's Next?</h2>
			<p class="mt-10">
				I'm looking for an internship opportunity to gain experience in doing REAL WORLD projects
			</p>
			<p class="text-center font-bold">Let's Work Together!</p>
		</div>
	</section>

	<div class="flex flex-col items-center mt-40 relative">
		<span class="absolute bottom-0 opacity-20 font-bold lg:text-[10rem] text-[5rem] oswald">REAL WORLD</span>
		<img class="ground h-[10vh] lg:h-auto" src={ground} alt="ground" />
	</div>
</div>

<style>
	.ground{
		filter: brightness(0%);
        object-fit: cover;
	}
</style>
 