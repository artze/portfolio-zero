<script>
	import '../reset.css';
	import '../style.css';
	import Artwork from '../components/artwork.svelte';
</script>

<svelte:head>
	<title>Arthur W</title>
	<script
		data-goatcounter="https://artze.goatcounter.com/count"
		async
		src="//gc.zgo.at/count.js"></script>
</svelte:head>

<div class="container">
	<div class="main">
		<div class="main__grid">
			<!-- Grid Control -->
			<!-- <div class="control-cell pos1-1" />
			<div class="control-cell pos2-1" />
			<div class="control-cell pos3-1" />
			<div class="control-cell pos1-2" />
			<div class="control-cell pos2-2" />
			<div class="control-cell pos3-2" />
			<div class="control-cell pos1-3" />
			<div class="control-cell pos2-3" />
			<div class="control-cell pos3-3" />
			<div class="control-cell pos1-4" />
			<div class="control-cell pos2-4" />
			<div class="control-cell pos3-4" /> -->

			<div class="brand">
				<span class="brand__text">Arthur W</span>
			</div>
			<slot />
		</div>
	</div>

	<div class="art" id="canvas">
		<Artwork />
	</div>

	<div class="nav">
		<div class="nav__grid">
			<!-- Grid Control -->
			<!-- <div class="control-cell pos1-1" />
			<div class="control-cell pos1-2" />
			<div class="control-cell pos1-3" />
			<div class="control-cell pos1-4" /> -->

			<div class="nav-menu">
				<div class="nav-menu__item">
					<a href="/" class="nav-menu__text">Home</a>
				</div>
				<div class="nav-menu__item">
					<a href="/about" class="nav-menu__text">About</a>
				</div>
				<div class="nav-menu__item">
					<a href="/keywords" class="nav-menu__text">Keywords</a>
				</div>
				<div class="nav-menu__item">
					<a href="/contact" class="nav-menu__text">Contact</a>
				</div>
				<div class="nav-menu__item">
					<a href="https://journal.artze.xyz" class="nav-menu__text" target="_blank">Journal</a>
				</div>
			</div>
		</div>
	</div>
</div>
