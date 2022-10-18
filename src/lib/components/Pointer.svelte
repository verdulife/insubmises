<script>
	import { onMount } from 'svelte';

	onMount(() => {
		const spotlight = document.querySelector('.spotlight');

		window.addEventListener('mousemove', (e) => {
			const { clientX, clientY } = e;

			console.dir(spotlight);

			spotlight.style.cssText = `
        top: ${clientY}px;
        left: ${clientX}px;
      `;
		});
	});
</script>

<span class="spotlight" />
<span class="closed" />

<style lang="scss">
	span {
		pointer-events: none;
	}

	.spotlight {
		position: fixed;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
		width: 8000px;
		height: 8000px;
		background: radial-gradient(rgba(#000, 0), rgba(#000, 0.9) 25%, #000 40%);
	}

	.closed {
		position: fixed;
		inset: 0;
		background: #000;
		animation: fadeOut 2s ease-in 1s forwards;
	}

	@keyframes fadeOut {
		to {
			opacity: 0;
		}
	}
</style>
