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
			Nuestra propuesta educativa consta de tres partes. Lorem ipsum dolor, sit amet consectetur
			adipisicing elit. Quos repellat porro alias ipsa? Saepe sed quis et perferendis magni fugit
			quae quos facilis qui soluta, eaque nisi architecto hic ex.
		</p>
	</div>

	<ul class="row jcenter">
		<li>
			<article class="col fcenter">
				<img src="cross.svg" alt="Espectáculo de danza" />
				<h3 class="title tcenter">Espectáculo de danza</h3>
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

		.content {
			max-width: 900px;
		}

		p {
			font-size: 22px;
		}
	}

	#welcome {
		background: url('/bg.jpg') no-repeat center;
		background-size: 80%;
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
			width: 1200px;
			aspect-ratio: 16/9;
			max-width: 80%;
			margin-top: 40px;
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
			}

			p {
				margin-top: 20px;
			}
		}

		ul {
			gap: 100px;
			margin-top: 150px;

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
		}
	}

	#about {
		background: url('/about.jpg') no-repeat center;
		background-size: cover;
		color: var(--color-text);

		article {
			h2 {
				font-size: 80px;
				font-weight: lighter;

				strong {
					font-weight: lighter;
					color: var(--color-pri);
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
