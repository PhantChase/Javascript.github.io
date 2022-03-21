# DRAWING ON CANVAS

## SVG

```
<p>Normal HTML.</p>
<svg xmlns="http://www.w3.org/2000/svg">
	<circle r="50" cx="50" cy="50" fill="red" />
	<rect x=120" y="5" width="90" height="90" stroke="blue fill="none" />
</svg>
```

## The Canvas Element

## Lines and Surfaces
```
<canvas></canvas>
<script>
	let cx = document.querySelector("canvas").getContext("2d");
	cx.strokeStyle = "blue";
	cx.strokeRect(5, 5, 50, 50);
	cx.lineWidth = 5;
	cx.strokeRect(135, 5, 50, 50);
</script>
```
## Paths
```
<canvas></canvas>
<script>
let cx = document.querySelector("canvas").getContext("2d");
cx.beginPath();
for (let y = 10; y < 100; y += 10) {
cx.moveTo(10, y);
cx.lineTo(90, y);
}
cx.stroke();
</script>
```
## Drawing a Pie Chart
```
const results = [
{name: "Satisfied", count: 1043, color: "lightblue"},
{name: "Neutral", count: 563, color: "lightgreen"},
{name: "Unsatisfied", count: 510, color: "pink"},
{name: "No comment", count: 175, color: "silver"}
];
```
## Text
```
<canvas></canvas>
<script>
let cx = document.querySelector("canvas").getContext("2d");
cx.font = "28px Georgia";
cx.fillStyle = "fuchsia";
cx.fillText("I can draw text, too!", 10, 50);
</script>
```
## Images
```
<canvas></canvas>
<script>
let cx = document.querySelector("canvas").getContext("2d");
let img = document.createElement("img");
img.src = "img/hat.png";
img.addEventListener("load", () => {
for (let x = 10; x < 200; x += 30) {
cx.drawImage(img, x, 10);
}
});
</script>
```
## Transformation
## Choosing a Graphics Interface