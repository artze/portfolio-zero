<div class="home">
	<span class="home__text">Software Engineer</span>
	<span class="home__text">Designer</span>
</div>
<div class="decorative-horizontal">
	<div class="decorative-horizontal__line" />
</div>
<div class="decorative-vertical">
	<div class="decorative-vertical__line" />
</div>

<style>
	.home {
		grid-column: 1 / span 3;
		grid-row: 3 / span 1;
	}

	.home__text {
		display: block;
		font-family: 'Gothic A1', sans-serif;
		font-size: 2.8rem;
		font-weight: 400;
		line-height: 1.42857142857;
	}

	.decorative-horizontal {
		align-self: end;
		grid-column: 2 / span 2;
		grid-row: 3 / span 1;
	}

	.decorative-horizontal__line {
		background-color: black;
		height: 1rem;
		width: 2fr;
	}

	.decorative-vertical {
		justify-self: end;
		grid-column: 2 / span 2;
		grid-row: 3 / span 1;
	}

	.decorative-vertical__line {
		background-color: black;
		height: 20.5761316872vh;
		width: 1rem;
	}
</style>
