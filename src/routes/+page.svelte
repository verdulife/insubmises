<script>
	import Mouse from '$lib/icons/Mouse.svelte';
</script>

<section id="welcome" class="viewport viewport">
	<a href="#presentation">
		<Mouse />
	</a>
</section>

<section id="presentation" class="col acenter xfill">
	<article class="content col acenter xfill">
		<h1 class="title tcenter">Un proyecto para la <strong>diversidad</strong></h1>

		<p class="tcenter">
			Presentamos esta propuesta conjunta, expresada en forma de danza contemporánea. Nace del deseo
			de visibilizar, desde una perspectiva feminista, una intromisión sistemática que sufrimos las
			mujeres en torno a la interiorización de nuestra propia imagen, que puede incidir sobre
			nuestra salud emocional y dificultar nuestro crecimiento como personas libres.
		</p>

		<a href="/proyecto" class="btn sec-outline">MÁS INFORMACIÓN</a>
	</article>
</section>

<section id="video" class="col acenter xfill">
	<h2 class="title tcenter">VIDEO PRESENTACIÓN</h2>

	<iframe
		src="https://player.vimeo.com/video/726970430?h=a92b00d11a&amp;title=0&amp;app_id=122963"
		frameborder="0"
		allow="autoplay; fullscreen; picture-in-picture"
		allowfullscreen=""
		title="(In)submises.mp4"
		data-ready="true"
	/>
</section>

<section id="educational" class="col acenter xfill">
	<div class="content">
		<h2 class="title tcenter">Propuesta <strong>educativa</strong></h2>

		<p class="tcenter">
			<strong>(in)Submises</strong> presenta una propuesta educativa transversal y basada en la experiencia
			personal. El espectáculo de danza es el punto de partida para adentrarse en la narrativa de la
			coreografía ligada al debate sobre las presiones de las redes sociales. La propuesta finaliza con
			un taller de movimiento y danza.
		</p>
	</div>

	<ul class="row jcenter">
		<li>
			<article class="col fcenter">
				<img src="cross.svg" alt="Espectáculo de danza" />
				<h3 class="title tcenter">Danza</h3>
				<p class="tcenter">
					Muestra en vivo de la coreografía <strong class="title">(in)Submises</strong> a los participantes
				</p>
			</article>
		</li>

		<li>
			<article class="col fcenter">
				<img src="cross.svg" alt="Espectáculo de danza" />
				<h3 class="title tcenter">Debate</h3>
				<p class="tcenter">
					Debate sobre la pieza expuesta y sobre las presiones de las redes sociales
				</p>
			</article>
		</li>

		<li>
			<article class="col fcenter">
				<img src="cross.svg" alt="Espectáculo de danza" />
				<h3 class="title tcenter">Taller</h3>
				<p class="tcenter">Puesta en práctiva con un taller de movimiento y danza</p>
			</article>
		</li>
	</ul>

	<a href="/propuesta-educativa" class="btn sec-outline">MÁS INFORMACIÓN</a>
</section>

<section id="about" class="col acenter fill">
	<article class="content col acenter xfill">
		<h2 class="title tcenter">Sobre <strong>nosotras</strong></h2>

		<p class="tcenter">
			Somos Sara y Gisela, dos bailarinas que, a pesar de tener cuerpos muy diferentes, hemos
			sufrido discriminación por nuestras interseccionalidades y queremos defender el poder de la
			sororidad. La coreografía es un reflejo de nuestra historia. Una historia de resiliencia.
		</p>
	</article>

	<a href="/nosotras" class="btn sec-outline">MÁS INFORMACIÓN</a>
</section>

<style lang="scss">
	section {
		padding: 200px 20px 0 20px;

		@media (max-width: 740px) {
			padding: 100px 20px 0 20px;
		}

		.content {
			max-width: 900px;

			@media (max-width: 980px) {
				max-width: 520px;
			}
		}

		p {
			font-size: 22px;

			@media (max-width: 740px) {
				font-size: 18px;
			}
		}
	}

	#welcome {
		background: url('/bg.jpg') no-repeat center;
		background-size: 80%;

		@media (max-width: 740px) {
			background-image: url('/bg-mobile.jpg');
		}
	}

	#presentation {
		color: var(--color-text);

		article {
			h1 {
				font-size: 80px;
				font-weight: lighter;

				strong {
					font-weight: lighter;
					color: var(--color-pri);
				}

				@media (max-width: 980px) {
					font-size: 60px;
				}

				@media (max-width: 740px) {
					font-size: 40px;
				}
			}

			p {
				margin-top: 20px;
			}

			a {
				font-weight: bold;
				margin-top: 40px;
			}
		}
	}

	#video {
		h2 {
			color: var(--color-sec);
			font-size: 24px;
			font-weight: lighter;
		}

		iframe {
			--video-width: 1200px;
			--video-max-width: 80%;

			width: var(--video-width);
			height: calc(var(--video-width) / 1.7777777778);
			max-width: 80%;
			max-height: calc(var(--video-max-width) / 1.7777777778);
			aspect-ratio: 16/9;
			margin-top: 40px;

			@media (max-width: 740px) {
				max-width: 100%;
				margin-top: 20px;
			}
		}
	}

	#educational {
		color: var(--color-text);

		.content {
			h2 {
				font-size: 60px;
				font-weight: lighter;

				strong {
					font-weight: lighter;
					color: var(--color-pri);
				}

				@media (max-width: 980px) {
					font-size: 40px;
				}

				@media (max-width: 740px) {
					font-size: 30px;
				}
			}

			p {
				margin-top: 20px;

				strong {
					font-family: var(--font-title);
					font-weight: lighter;
				}
			}
		}

		ul {
			gap: 100px;
			margin-top: 150px;

			@media (max-width: 980px) {
				gap: 200px;
				flex-direction: column;
			}

			@media (max-width: 740px) {
				gap: 150px;
				margin-top: 100px;
			}

			li {
				width: 100%;
				max-width: 350px;

				article {
					position: relative;

					*:not(img) {
						z-index: 1;
					}

					img {
						position: absolute;
						width: 200px;
					}

					h3 {
						font-weight: lighter;
						text-transform: uppercase;
						color: var(--color-sec);
					}

					p {
						font-size: 18px;
						margin-top: 20px;

						strong {
							font-weight: lighter;
						}
					}
				}
			}
		}

		a {
			font-weight: bold;
			margin-top: 150px;

			@media (max-width: 740px) {
				margin-top: 100px;
			}
		}
	}

	#about {
		background: url('/about.jpg') no-repeat center;
		background-size: cover;
		color: var(--color-text);

		@media (max-width: 980px) {
			background-position-x: 70%;
			background-position-y: bottom;
			background-size: 200%;
		}

		@media (max-width: 740px) {
			height: 80%;
			background-position-y: bottom;
			background-size: 200%;
		}

		@media (max-height: 740px) {
			height: 100%;
			background-position-y: bottom;
			background-size: 200%;
		}

		article {
			h2 {
				font-size: 60px;
				font-weight: lighter;

				strong {
					font-weight: lighter;
					color: var(--color-pri);
				}

				@media (max-width: 980px) {
					font-size: 40px;
				}

				@media (max-width: 740px) {
					font-size: 30px;
				}
			}

			p {
				margin-top: 20px;
			}
		}

		a {
			font-weight: bold;
			margin-top: 40px;
		}
	}
</style>
