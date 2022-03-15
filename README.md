# PART I
## THE SECRET L IFE OF OB JECTS
### Encapsulation
### Methods
```
let rabbit = {};
rabbit.speak = function(line) {
	console.log(`The rabbit says '${line}'`);
};

rabbit.speak("I'm alive."); // → The rabbit says 'I'm alive.'
```
### Prototypes
```
console.log(Object.getPrototypeOf(Math.max) ==
	Function.prototype);
// → true console.log(Object.getPrototypeOf([]) == Array.prototype);
// → true
```
### Classes
```
function makeRabbit(type) {
	let rabbit = Object.create(protoRabbit);
	rabbit.type = type;
	return rabbit;
}
```
### Class Notation
```
class Rabbit {
	constructor(type) {
		this.type = type;
	}
	speak(line) {
		console.log(`The ${this.type} rabbit says '${line}'`);
		}
	}
let killerRabbit = new Rabbit("killer");
let blackRabbit = new Rabbit("black");
```
###  Overriding Derived Properties
```
Rabbit.prototype.teeth = "small";
console.log(killerRabbit.teeth);
// → small
killerRabbit.teeth = "long, sharp, and bloody";
console.log(killerRabbit.teeth);
// → long, sharp, and bloody
console.log(blackRabbit.teeth);
// → small
console.log(Rabbit.prototype.teeth);
// → small
```
### Maps