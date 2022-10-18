<script>
	import { showState } from '$lib/stores';
	import { fade } from 'svelte/transition';
	import Logo from '$lib/icons/Logo.svelte';

	let menu = false;

	function togMenu() {
		menu = !menu;
	}
</script>

{#if $showState}
	<nav class="row jbetween acenter xfill" transition:fade={{ duration: 800 }}>
		<a class="logo" href="/">
			<Logo />
		</a>

		<img class:btn-close={menu} src="/cross.svg" alt="Menú" on:click={togMenu}/>

		<ul class="row" class:menu-open={menu}>
			<li class="row">
				<a href="/proyecto">PROYECTO</a>
			</li>
			<li class="row">
				<a href="/propuesta-educativa">PROPUESTA EDUCATIVA</a>
			</li>
			<li class="row">
				<a href="/nosotras">NOSOTRAS</a>
			</li>
			<li class="row">
				<a href="/contacto">CONTACTO</a>
			</li>
		</ul>
	</nav>

	<aside>
		<a
			class="row acenter"
			href="https://www.instagram.com/saracolomino/"
			target="_blank"
			rel="noreferrer"
		>
			Sara Colomino
		</a>

		<a
			class="row acenter"
			href="https://www.instagram.com/gisusgi/"
			target="_blank"
			rel="noreferrer"
		>
			Gisela de Paz Solvas
		</a>
	</aside>
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

		.logo {
			z-index: 1;
		}

		img {
			width: 40px;
			display: none;
			transform: rotate(45deg);
			padding: 10px;
			transition: 200ms;
			z-index: 1;

			@media (max-width: 980px) {
				display: flex;
			}
		}

		.btn-close {
			transform: rotate(0);
		}

		ul {
			gap: 40px;
			
			@media (max-width: 980px) {
				position: fixed;
				top: -200px;
				left: 0;
				width: 100%;
				height: 100%;
				flex-direction: column;
				justify-content: center;
				align-items: center;
				background: rgba(#000, 0.8);
				backdrop-filter: blur(10px);
				opacity: 0;
				pointer-events: none;
				padding: 40px;
				transition: 800ms;
			}
		}

		.menu-open {
			top: 0;
			opacity: 1;
			pointer-events: all;
		}

		@media (max-width: 980px) {
			li {
				width: 100%;
				justify-content: center;
			}
		}

		a:not(.logo) {
			font-family: var(--font-title);
			color: var(--color-text);
			transition: 200ms;

			&:hover {
				color: var(--color-pri);
			}

			@media (max-width: 980px) {
				font-size: 40px;
				text-align: center;
			}
			
			@media (max-width: 740px) {
				font-size: 26px;
				text-align: center;
			}
		}
	}

	aside {
		color: var(--color-text);

		a {
			position: fixed;
			top: 50%;
			transform: translateY(-50%) rotate(180deg);
			writing-mode: vertical-lr;
			font-family: var(--font-title);
			text-transform: uppercase;
			padding: 20px;

			&:first-of-type {
				left: 0;
			}

			&:last-of-type {
				right: 0;
			}

			&:before,
			&:after {
				content: '';
				width: 1px;
				height: 40px;
				display: flex;
				background: var(--color-text);
				margin: 20px 0;
			}
		}

		@media (max-width: 740px) {
			display: none;
		}
	}
</style>
