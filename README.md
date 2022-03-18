# PART I
## THE DOCUMENT OB JECT MODEL
### Document Structure
### Trees
### The Standard
### Moving Through the Tree
### Finding Elements
```
let link = document.body.getElementsByTagName("a")[0];
console.log(link.href);
```
### Changing the Document
```
<p>One</p>
<p>Two</p>
<p>Three</p>

<script>
	let paragraphs = document.body.getElementsByTagName("p");
	document.body.insertBefore(paragraphs[2], paragraphs[0]);
</script>
```
### Creating Nodes
```
let arrayish = {0: "one", 1: "two", length: 2};
let array = Array.from(arrayish);
console.log(array.map(s => s.toUpperCase()));
// → ["ONE", "TWO"]
```
### Attributes
```
<p data-classified="secret">The launch code is 00000000.</p>
<p data-classified="unclassified">I have two feet.</p>
<script>
let paras = document.body.getElementsByTagName("p"); for (let para of Array.from(paras)) {
	if (para.getAttribute("data-classified") == "secret") {
		para.remove();
	}
}
</script>
```
### Layout
