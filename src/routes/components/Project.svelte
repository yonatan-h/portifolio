<script>
	export let title = 'title';
	export let id = 'id';
	export let link = '';
	export let sentences = ['sentence1', 'sentence2'];
	export let technologies = [];
	export let imageSrc = '';
</script>

<section {id} class="flex flex-col lg:flex-row justify-between gap-5">
	<div class="backdrop-blur max-w-sm ">
		<h2 class="text-4xl oswald">
			<a class={link?"underline":''} href={link}>
				{title}
			</a>
		</h2>
		<ul class="mt-5">
			{#each sentences as sentence}
				<li>{@html sentence}</li>
			{/each}

			{#if technologies.length}
				<li>
					<ul class="flex flex-wrap gap-2">
						{#each technologies as tech}
							<li class="bg-white text-black px-2 rounded list-none">{tech}</li>
						{/each}
					</ul>
				</li>
			{/if}
		</ul>
	</div>
	<img src={imageSrc} alt={title} class="rounded-md lg:max-w-[40vw] backdrop-blur object-cover" />
</section>
