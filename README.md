# PART I
## DATA STRUCTURES: OB JECTS AND ARRAYS
### The Weresquirrel
### Data Sets
```
let listOfNumbers = [2, 3, 5, 7, 11];
console.log(listOfNumbers[2]); // → 5
console.log(listOfNumbers[0]); // → 2
console.log(listOfNumbers[2 - 1]); // → 3
```
### Properties
```
null.length;
// → TypeError: null has no properties
```
### Methods
```
let sequence = [1, 2, 3];
sequence.push(4);
sequence.push(5);
console.log(sequence); // → [1, 2, 3, 4, 5]
console.log(sequence.pop()); // → 5
console.log(sequence); // → [1, 2, 3, 4]
```
### Objects
```
let descriptions = {
	work: "Went to work", "touched tree": "Touched a tree"
};
```
###  Mutability
```
let object1 = {value: 10};
let object2 = object1;
let object3 = {value: 10};
console.log(object1 == object2); // → true
console.log(object1 == object3); // → false
object1.value = 15;
console.log(object2.value); // → 15
console.log(object3.value); // → 10
```
### Computing Correlation
```
function phi(table) {
return (table[3] * table[0] - table[2] * table[1]) /
Math.sqrt((table[2] + table[3]) * (table[0] + table[1]) * (table[1] + table[3]) * (table[0] + table[2]));
}
console.log(phi([76, 9, 4, 1])); // → 0.068599434
```
### Array Loops
```
for (let i = 0; i < JOURNAL.length; i++) {
	let entry = JOURNAL[i]; // Do something with entry
}
```
### The Final Analysis
### Further Arrayology