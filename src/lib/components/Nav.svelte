<script>
	import { showState } from '$lib/stores';
	import { fade } from 'svelte/transition';
	import Logo from '$lib/icons/Logo.svelte';
</script>

{#if $showState}
	<nav class="row jbetween acenter xfill" transition:fade={{ duration: 800 }}>
		<a href="/">
			<Logo />
		</a>

		<ul class="row">
			<li>
				<a href="/proyecto">PROYECTO</a>
			</li>
			<li>
				<a href="/propuesta-educativa">PROPUESTA EDUCATIVA</a>
			</li>
			<li>
				<a href="/nosotras">NOSOTRAS</a>
			</li>
			<li>
				<a href="/contacto">CONTACTO</a>
			</li>
		</ul>
	</nav>
{/if}

<style lang="scss">
	nav {
		position: fixed;
		top: 0;
		left: 0;
		right: 0;
		max-width: 1600px;
		background: linear-gradient(to bottom, #000, rgba(#000, 0.3) 70%, rgba(#000, 0));
		margin: 0 auto;
		padding: 40px;
		z-index: 99;

		ul {
			gap: 40px;
		}

		a {
			font-family: var(--font-title);
			color: var(--color-text);
			transition: 200ms;

			&:hover {
				color: var(--color-pri);
			}
		}
	}
</style>
