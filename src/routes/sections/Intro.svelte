<script>
	import Star from '../components/Star.svelte';

	import phone from '$lib/assets/phone.svg';
	import email from '$lib/assets/email.svg';
	import github from '$lib/assets/github.svg';
	import linkedIn from '$lib/assets/linkedin.svg';
	import codeForces from '$lib/assets/codeforces.svg';
	import leetCode from '$lib/assets/leetcode.svg';

	const positions = [];
	for (let i = 0; i < 100; i++) {
		const x = Math.floor(Math.random() * 100);
		const y = Math.floor(Math.random() * 100);
		positions.push([x, y]);
	}
</script>

<div id="intro" class="sec-container relative space-dark">
	{#each positions as [x, y]}
		<Star {x} {y} wait={true} fuzzy={false} />
	{/each}

	<section class="flex flex-col justify-center items-center">
		<div class="backdrop-blur max-w-md pt-40">
			<h1 class="text-6xl lg:text-7xl oswald text-center">Hi, Its Yonatan</h1>
			<p class="mt-10 text-center">
				A Software engineering student based in Addis Ababa, Ethiopia. Seeking to solve problems in the <b>REAL WORLD</b>.
			</p>

			<ul class="links mt-10">
				<div class="flex flex-wrap gap-5 justify-center">
					<li>Name: Yonatan Haile Demisse</li>
					<li><img src={phone} alt="phone" />+251911991199</li>
					<li><img src={email} alt="email" /> yonatanhaile.y@gmail.com</li>
					
					<li>
						<a href="https://github.com/yonatan-h/">
							<img src={github} alt="gitHub" />
							GitHub</a
						>
					</li>
					<li>
						<a href="https://www.linkedin.com/in/yonatan-haile-demisse/">
							<img src={linkedIn} alt="linkedIn" />
							LinkedIn</a
						>
					</li>

					<li>
						<a href="https://leetcode.com/yonatan-h/">
							<img src={leetCode} alt="leetCode" />
							LeetCode</a
						>
					</li>
					<li>
						<a href="https://codeforces.com/profile/yonatan-h">
							<img src={codeForces} alt="codeForces" />
							Codeforces</a
						>
					</li>
				</div>
			</ul>
		</div>
	</section>
</div>

<style>
	li img {
		display: inline-block;
	}
	li {
		list-style: none;
		display: flex;
		gap: 10px;
		padding: 5px;
		border-radius: 5px;
		background-color: rgba(255, 255, 255, 0.2);
	}
</style>
