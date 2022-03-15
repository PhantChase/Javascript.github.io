# PART I
## HIGHER-ORDER FUNCTIONS
### Abstraction
### Abstracting Repetition
```
let labels = []; repeat(5, i => {
labels.push(`Unit ${i + 1}`); }); console.log(labels); // → ["Unit 1", "Unit 2", "Unit 3", "Unit 4", "Unit 5"]
```
### Higher-Order Functions
```
function noisy(f) {
	return (...args) => {
		console.log("calling with", args);
		let result = f(...args);
		console.log("called with", args, ", returned", result);
		return result;
	};
}
noisy(Math.min)(3, 2, 1);
// → calling with [3, 2, 1]
// → called with [3, 2, 1] , returned 1
```
### Script Data Set
```
{
	name: "Coptic",
	ranges: [[994, 1008], [11392, 11508], [11513, 11520]],
	direction: "ltr", year: -200,
	living: false,
	link:"https://en.wikipedia.org/wiki/Coptic_alphabet"
}
```
### Filtering Arrays
```
function filter(array, test) {
	let passed = [];
	for (let element of array) {
		if (test(element)) {
			passed.push(element);
		}
	} return passed;
}

console.log(filter(SCRIPTS, script => script.living));
// → [{name: "Adlam", ...}, ...]
```
###  Transforming with map
```
function map(array, transform) {
	let mapped = [];
	for (let element of array) {
		mapped.push(transform(element));
	}
	return mapped;
}
let rtlScripts = SCRIPTS.filter(s => s.direction == "rtl");
console.log(map(rtlScripts, s => s.name));
// → ["Adlam", "Arabic", "Imperial Aramaic", ...]
```
### Summarizing with reduce