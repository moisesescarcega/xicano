<script>
	let elemCarousel;

	function carouselLeft() {
		const x =
			elemCarousel.scrollLeft === 0
				? elemCarousel.clientWidth * elemCarousel.childElementCount // loop
				: elemCarousel.scrollLeft - elemCarousel.clientWidth; // step left
		elemCarousel.scroll(x, 0);
	}

	function carouselRight() {
		const x =
			elemCarousel.scrollLeft === elemCarousel.scrollWidth - elemCarousel.clientWidth
				? 0 // loop
				: elemCarousel.scrollLeft + elemCarousel.clientWidth; // step right
		elemCarousel.scroll(x, 0);
	}

	function carouselThumbnail(index) {
		elemCarousel.scroll(elemCarousel.clientWidth * index, 0);
	}
					
</script>

<div class="w-screen h-screen lg:h-[48rem] bg-[url('vista_interior_pb_rio_sur.jpg')] bg-cover bg-fixed bg-center grid content-center space-y-4">
	<h1 class="text-center drop-shadow-sm p-6" style="font-family: 'Oleo Script'; font-size:6rem">Xicano</h1>
	<h3 class="h3 text-center drop-shadow-sm">Experiencia gastronómica en la frontera</h3>
	<a href="#descripcion" class="btn btn-lg variant-glass-primary w-60 h4 place-self-center">Conoce el proyecto</a>
</div>

<div class="container mx-auto">
	<section class="grid-cols-1 w-full bg-gradient-to-br variant-gradient-tertiary-primary" id="descripcion">
		<div class="grid grid-rows-1 grid-flow-row lg:grid-flow-col gap-6 mb-12 py-8 content-center">

			<div class="place-self-center mx-8">
				<img
					alt="Vista del proyecto"
					src="version_anteproyectoaaa.jpg"
					class="h-fit w-lg object-cover mx-auto rounded-lg shadow-lg"
				/>
			</div>

			<div class="text-center col-span-1 place-self-center lg:col-span-2 w-full lg:w-3/5 space-y-2">
				<h1 class="text-3xl font-bold">Un restaurante en la primera esquina de México</h1>
				<img
					alt="La primera esquina de México"
					src="localizacion_xicano.jpg"
					class="h-80 w-lg object-cover mx-auto rounded-lg shadow-lg"
				/>
				<a href="#planos" class="btn btn-lg variant-filled-secondary w-60 h4 place-self-center">Plantas arquitectónicas</a>
			</div>

		</div>
	</section>

	<section class="grid-cols-1 w-full">
		<div class="grid grid-rows-1 grid-flow-row lg:grid-flow-col gap-6 mb-12">

			<div class="text-center col-span-1 place-self-center lg:col-span-2 w-full lg:w-3/5">
				<h1 class="text-3xl font-bold">Un proyecto versátil</h1>
				<p class="py-4">
					Tomando como prioridad la luz, autonomía energética, optimización climática y un programa arquitectónico modular por pisos que ayudan a un crecimiento eficiente del proyecto y la posibilidad de extenderlo exitosamente.
				</p>
				<p class="py-6">
					Un lugar emblemático con vista al Río Bravo y a la Gran Plaza.
				</p>
			</div>

			<div class="place-self-center mx-8">
				<img
					alt="Vista del proyecto desde el Río Bravo"
					src="version_anteproyectobb.jpg"
					class="h-fit w-lg object-cover mx-auto rounded-lg shadow-lg"
				/>
			</div>

		</div>
	</section>

	<section class="w-full variant-soft-primary bg-[url('slide1.jpg')] bg-cover bg-fixed bg-center grid">
		<div class="grid grid-rows-1 gap-6 mb-12 py-8">
			<div class="text-center col-span-1 place-self-center w-full">
				<h1 class="text-center text-6xl drop-shadow-sm p-6" style="font-family: 'Oleo Script';">Un nuevo hito en el corazón de la frontera</h1>
				<p class="py-6 w-3/5 text-center mx-auto">Revivir el corazón de Piedras Negras, revitalizando su centro histórico y ofreciendo una experiencia única tanto al orgulloso nigropetense como al visitante que busca una opción diferente en este lado de la frontera.
				</p>
			</div>
		</div>
	</section>

	<section class="grid grid-cols-1 md:grid-cols-2 gap-2 py-4">
		<div class="grid gap-4">
			<div>
				<img class="h-auto max-w-full rounded-lg" src="vista_interior_pb_rio_norte.jpg" alt="Vista interior norte" />
			</div>
			<div>
				<img class="h-auto max-w-full rounded-lg" src="vista_interior_pb_rio_sur.jpg" alt="Vista interior norte" />
			</div>
		</div>
		<div class="grid gap-4">
			<div>
				<img class="h-auto max-w-full rounded-lg" src="vista_interior_privado_bandera.jpg" alt="Vista interior norte" />
			</div>
			<div>
				<img class="h-auto max-w-full rounded-lg" src="vista_interior_oficina_pa.jpg" alt="Vista interior norte" />
			</div>
		</div>
		<div class="grid gap-4">
			<div>
				<img class="h-auto max-w-full rounded-lg" src="estudio_volumetrico_mi-Imagen8.jpg" alt="Vista interior norte" />
			</div>
			<div>
				<img class="h-auto max-w-full rounded-lg" src="bar_terraza_sur.jpg" alt="Vista interior norte" />
			</div>
		</div>
		<div class="grid gap-4">
			<div>
				<img class="h-auto max-w-full rounded-lg" src="corte_longitudinal_g.jpg" alt="Vista interior norte" />
			</div>
			<div>
				<img class="h-auto max-w-full rounded-lg" src="corte_transversal_g.jpg" alt="Vista interior norte" />
			</div>
		</div>
	</section>

	<section id="planos">
		<div class="card p-4 grid grid-cols-[auto_1fr_auto] gap-4 items-center">
			<!-- Button: Left -->
			<button type="button" class="btn-icon variant-filled" on:click={carouselLeft}>
				<p class="text-lg font-bold">&larr;</p>
			</button>
			<!-- Full Images -->
			<div bind:this={elemCarousel} class="snap-x snap-mandatory scroll-smooth flex overflow-x-auto">
					<img
						class="snap-center w-fit rounded-container-token"
						src="a-01-scaled.jpg"
						alt="planta"
						loading="lazy"
					/>
					<img
						class="snap-center w-fit rounded-container-token"
						src="a-02-scaled.jpg"
						alt="planta"
						loading="lazy"
					/>
					<img
						class="snap-center w-fit rounded-container-token"
						src="a-03-scaled.jpg"
						alt="planta"
						loading="lazy"
					/>
					<img
						class="snap-center w-fit rounded-container-token"
						src="a-04-scaled.jpg"
						alt="planta"
						loading="lazy"
					/>
					<img
						class="snap-center w-fit rounded-container-token"
						src="a-07-scaled.jpg"
						alt="planta"
						loading="lazy"
					/>
					<img
						class="snap-center w-fit rounded-container-token"
						src="a-09-scaled.jpg"
						alt="planta"
						loading="lazy"
					/>
			</div>
			<!-- Button: Right -->
			<button type="button" class="btn-icon variant-filled" on:click={carouselRight}>
				<p class="text-lg font-bold">&rarr;</p>
			</button>
		</div>

		<div class="card p-4 grid grid-cols-6 gap-4 mt-2">
				<button type="button" on:click={() => carouselThumbnail(0)}>
					<img
						class="rounded-container-token"
						src="a-01-scaled.jpg"
						alt="planta"
						loading="lazy"
					/>
				</button>
				<button type="button" on:click={() => carouselThumbnail(1)}>
					<img
						class="rounded-container-token"
						src="a-02-scaled.jpg"
						alt="planta"
						loading="lazy"
					/>
				</button>
				<button type="button" on:click={() => carouselThumbnail(2)}>
					<img
						class="rounded-container-token"
						src="a-03-scaled.jpg"
						alt="planta"
						loading="lazy"
					/>
				</button>
				<button type="button" on:click={() => carouselThumbnail(3)}>
					<img
						class="rounded-container-token"
						src="a-04-scaled.jpg"
						alt="planta"
						loading="lazy"
					/>
				</button>
				<button type="button" on:click={() => carouselThumbnail(4)}>
					<img
						class="rounded-container-token"
						src="a-07-scaled.jpg"
						alt="planta"
						loading="lazy"
					/>
				</button>
				<button type="button" on:click={() => carouselThumbnail(5)}>
					<img
						class="rounded-container-token"
						src="a-09-scaled.jpg"
						alt="planta"
						loading="lazy"
					/>
				</button>
		</div>
	</section>
</div>