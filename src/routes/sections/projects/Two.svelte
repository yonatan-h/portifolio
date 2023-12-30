
<script>
	import Project from '../../components/Project.svelte';
	import mirkusve from '$lib/assets/mirkusve.png'
</script>

<div class="sec-container night-to-day">
	<section>
		<Project
		title={'#2 Mirkusve'}
		id={'mirkusve'}
		link={'https://github.com/yonatan-h/mirkusve2'}
		imageSrc={mirkusve}
		sentences={[
			`After answering a LeetCode question, I had to upload the answer code to GitHub and then attach it in A2SV's Google Sheets. It was tiresome.`,
			'Mirkusve is a Chrome Extension that automates this process for A2SV students.'
		]}
		technologies={['React.js', 'Google Apps Script', 'GitHub Apps', 'Chrome Extensions']}
	/>


	</section>
</div>

<style>
	.night-to-day{
		background: linear-gradient(var(--night-blue), var(--morning-sky));
	}
</style>