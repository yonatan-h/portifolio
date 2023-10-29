<script>
	import cloud from '$lib/assets/cloud.svg';
	export let x;
	export let y;
	export let duration;

	const style = `
        top: ${y}%;
        left:${x}%;
        animation-duration: ${duration}s;
    `;
</script>

<img src={cloud} {style} alt="cloud decoration" />

<style>
	img {
		position: absolute;
		width: 100px;
		opacity: 0.2;

		animation-timing-function: linear;
		animation-iteration-count: infinite;
		animation-name: move;
	}

	@keyframes move {
		0% {
			transform: translateX(0px);
		}

		50% {
			transform: translateX(-100vw);
			animation-timing-function: step-end;
		}

		51% {
			transform: translateX(100vw);
		}
	}
</style>
