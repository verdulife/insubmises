<footer class="row fcenter xfill">
	<img src="logo-red.svg" alt="(in)Submises" />

	<ul class="row">
		<li>
			<h4>LLAMAR</h4>
			<a href="tel:0034680790253">(+34) 680.790.253</a>
		</li>

		<li>
			<h4>EMAIL</h4>
			<a href="mailto:gigi_zap@hotmail.com">gigi_zap@hotmail.com</a>
		</li>

		<li>
			<h4>SÍGUENOS EN INSTAGRAM</h4>

			<ul class="social col xfill">
				<li class="xfill">
					<a href="https://www.instagram.com/saracolomino/" target="_blank" rel="noreferrer"
						>Sara Colomino</a
					>
				</li>
				<li class="xfill">
					<a href="https://www.instagram.com/gisusgi/" target="_blank" rel="noreferrer"
						>Gisela de Paz Solvas</a
					>
				</li>
			</ul>
		</li>

		<li>
			<h4>DIRECCIÓN</h4>
			<a href="https://goo.gl/maps/xKa5VPyu5dcYzLrr6" target="_blank" rel="noreferrer"
				>Ludwigstraße 53, 04315 Leipzig, Alemania</a
			>
		</li>
	</ul>
</footer>

<style lang="scss">
	footer {
		max-width: 1600px;
		background: var(--color-sec);
		color: var(--color-text);
		margin: 100px auto 0 auto;
		padding: 60px 40px;
		
		@media (max-width: 980px) {
			justify-content: flex-start;
			gap: 60px;
			margin: 0 auto;
		}

		img {
			width: 200px;
		}

		ul:not(.social) {
			gap: 60px;
			margin-left: 100px;
			
			@media (max-width: 980px) {
				gap: 40px;
				margin-left: 0;
			}
		}
	}
</style>
