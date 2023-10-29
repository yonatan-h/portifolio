<script>
	export let x = 50;
	export let y = 50;
	export let wait = false;
	export let fuzzy = true;

	const position = `position: absolute; top:${y}%; left:${x}%;`
	const shadow = (fuzzy?'':'box-shadow:none;')
	let visible = wait? false : true

	setTimeout(() => (visible = true), Math.random() * 2000);
</script>

{#if visible}
	<div class="star" style={position + shadow } />
{/if}

<style>
	.star {
		--size: 4px;
		width: var(--size);
		height: var(--size);
		opacity: 0.4;
		box-shadow: 0 0 9px 1.5px white;
		border-radius: 100%;
		animation: twinkle 100ms infinite alternate-reverse;




	}

	@keyframes twinkle {
		0% {
			background-color: rgba(255, 255, 255, 0.5);
		}

		100% {
			background-color: white;
		}
	}
</style>
