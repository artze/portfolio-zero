<script>
	import '../reset.css';
	import '../style.css';
</script>

<div class="container">
	<div class="main">
		<div class="main__grid">
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
			<slot />
		</div>
	</div>
	<div class="art" />
	<div class="nav">
		<div class="nav__grid">
			<div class="control-cell pos1-1" />
			<div class="control-cell pos1-2" />
			<div class="control-cell pos1-3" />
			<div class="control-cell pos1-4" />
		</div>
	</div>
</div>
