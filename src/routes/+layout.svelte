<script>
	import { showState } from '$lib/stores';
	import Nav from '$lib/components/Nav.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import Pointer from '$lib/components/Pointer.svelte';

	setTimeout(() => {
		$showState = true;
	}, 2000);
</script>

<main class="scroll">
	<Nav />
	<slot />
	<Footer />
</main>

<Pointer />

<style lang="scss">
	@import 'https://cdn.jsdelivr.net/gh/verdulife/utility-classes/dist/reset.css';
	@import 'https://cdn.jsdelivr.net/gh/verdulife/utility-classes/dist/utility-classes.css';

	:root {
		--color-pri: #ff005e;
		--color-sec: #2e272a;
		--color-text: #c9b6bc;
	}

	.scroll {
		background: #000;
	}

	::-webkit-scrollbar-track {
		background: #000;
	}
</style>
