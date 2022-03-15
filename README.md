# PART I
## BUGS AND ERRORS
### Language
### Strict Mode
```
function canYouSpotTheProblem() {
	"use strict";
	for (counter = 0; counter < 10; counter++) {
		console.log("Happy happy");
	}
}

canYouSpotTheProblem();
// → ReferenceError: counter is not defined
```
### Types
```
// (VillageState, Array) → {direction: string, memory: Array}
function goalOrientedRobot(state, memory) {
	// ...
}
```
### Testing
### Debugging
### Error Propagation
```
function lastElement(array) {
	if (array.length == 0) {
		return {failed: true};
	} else {
		return {element: array[array.length - 1]};
	}
}
```
### Exceptions