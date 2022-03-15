# PART I
## FUNCTIONS
### Defining a Function
```
const square = function(x) { 
	return x * x; 
}; 
console.log(square(12)); // → 144
```
### Functions as Values
```
let launchMissiles = function() {
	missileSystem.launch("now"); 
}; 
if (safeMode) {
	launchMissiles = function() {/* do nothing */};
}
```
### Declaration Notation
### Arrow Functions
```
const power = (base, exponent) => { let result = 1; for (let count = 0; count < exponent; count++) { result *= base; } return result; };
```
###  The Call Stack
```
function chicken(){
	return egg();
} function egg() {
	return chicken();
}
console.log(chicken() + " came first."); // → ??
```
### Optional Arguments
```
function square(x) {
	return x * x;
}
console.log(square(4, true, "hedgehog")); // → 16
```
