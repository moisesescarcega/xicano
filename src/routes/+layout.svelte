<script>
	import '../app.postcss';
	import { AppShell, AppBar } from '@skeletonlabs/skeleton';
</script>

<AppShell regionPage="relative" slotPageHeader="sticky top-0 z-10">

	<svelte:fragment slot="header">
		
		<AppBar gridColumns="grid-cols-3" slotDefault="place-self-center" slotTrail="place-content-end">
			<svelte:fragment slot="lead">
				<a href="/"><img src="x_logo.png" width="32" alt="logo Xicano" /></a>
			</svelte:fragment>
				<h1 style="font-family: 'Oleo Script';" class="h4">Xicano</h1>
			<svelte:fragment slot="trail">
				<a href="#descripcion">Proyecto</a>
				<p> | </p>
				<a href="#planos">Planos</a>
			</svelte:fragment>
		</AppBar>

		
	</svelte:fragment>
	
	<slot />

	<svelte:fragment slot="pageFooter">
		<div class="grid-cols-2 w-full mt-6 p-12 variant-soft-surface">
			<p>Todos los derechos reservados &copy; 2020. Laboratorio de Urbanismo y Planeación Ambiental LUPA S.A. de C.V.</p>
			<p>Proyecto: Arq. Jorge Ponce, Arq. Moisés Escárcega</p>
			<a href="https://mescarcega.vercel.app/">https://mescarcega.vercel.app/</a>
		</div>
	</svelte:fragment>

</AppShell>
