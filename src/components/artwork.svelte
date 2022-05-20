<script>
	import P5 from 'p5-svelte';

	const config = {
		numOfTriangles: 25,
		colors: ['#252525', '#29A340', '#2BAAD7', '#EF0F8B', '#F11404']
	};

	const getRandomFromArr = (arr) => {
		return arr[Math.floor(Math.random() * arr.length)];
	};

	function initTriangle(p) {
		const rotationDeg = [90, 180, 270];
		const scrollAmount = [9, 16, 25];
		return class Triangle {
			constructor() {
				this.fillColor = p.color(getRandomFromArr(config.colors));
				this.rotateAngle = getRandomFromArr(rotationDeg);
				this.sideLength = 324;
				this.yOffset = p.random(-p.height, p.height);
				this.scrollAmount = getRandomFromArr(scrollAmount);
			}

			update(delta) {
				if (delta > 0) {
					this.yOffset += this.scrollAmount;
				} else {
					this.yOffset -= this.scrollAmount;
				}
				if (this.yOffset > p.height) {
					this.yOffset = -p.height;
				} else if (this.yOffset < -p.height) {
					this.yOffset = p.height;
				}
			}

			draw() {
				p.push();
				p.noStroke();
				p.fill(this.fillColor);
				p.translate(0, this.yOffset);
				p.translate(this.sideLength / 2, this.sideLength / 2);
				p.rotate(this.rotateAngle);
				p.triangle(
					-this.sideLength / 2,
					this.sideLength / 2,
					-this.sideLength / 2,
					-this.sideLength / 2,
					this.sideLength / 2,
					this.sideLength / 2
				);
				p.pop();
			}
		};
	}

	const sketch = (p5) => {
		p5.setup = () => {
			p5.createCanvas(324, p5.windowHeight);
			p5.noLoop();
			p5.mouseClicked = () => {
				p5.clear();
				p5.redraw();
			};
			p5.angleMode(p5.DEGREES);
		};
		p5.draw = () => {
			p5.background('#f9e9ea');
			const Triangle = initTriangle(p5);
			const triangles = [];
			for (let i = 0; i < config.numOfTriangles; i++) {
				const triangle = new Triangle();
				triangle.draw();
				triangles.push(triangle);
			}
			p5.mouseWheel = (e) => {
				p5.clear();
				p5.background('#f9e9ea');
				triangles.forEach((t) => {
					t.update(e.delta);
					t.draw();
				});
			};
		};
	};
</script>

<P5 {sketch} />
