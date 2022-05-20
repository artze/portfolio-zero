<script>
	import '../reset.css';
	import '../style.css';
</script>

<div class="container">
	<div class="main">
		<div class="main__grid">
			<!-- Grid Control -->
			<div class="control-cell pos1-1" />
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
			<div class="control-cell pos3-4" />

			<div class="brand">
				<span class="brand__text">Arthur W</span>
			</div>
			<slot />
		</div>
	</div>
	<div class="art" />
	<div class="nav">
		<div class="nav__grid">
			<!-- Grid Control -->
			<div class="control-cell pos1-1" />
			<div class="control-cell pos1-2" />
			<div class="control-cell pos1-3" />
			<div class="control-cell pos1-4" />

			<div class="nav-menu">
				<span class="nav-menu__text">Home</span>
				<span class="nav-menu__text">About</span>
				<span class="nav-menu__text">Contact</span>
				<span class="nav-menu__text">Journal</span>
			</div>
		</div>
	</div>
</div>
