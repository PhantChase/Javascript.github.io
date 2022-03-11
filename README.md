# PART I
## PROGRAM STRUCTURE
### Expressions and Statements
```
1; !false;
```
### Bindings
```
let caught = 5 * 5;
let ten = 10;
console.log(ten * ten); // → 100
```
### Binding Names
```
break case catch class const continue debugger default
delete do else enum export extends false finally for
function if implements import interface in instanceof let new package private protected public return static super switch this throw true try typeof var void while with yield
```
### The Environment
### Functions
```
prompt("Enter passcode");
```
###  The console.log Function
### Return Values
```
console.log(Math.max(2, 4)); // → 4
```
### Control Flow
```
let theNumber = Number(prompt("Pick a number"));
console.log("Your number is the square root of " + theNumber * theNumber);
```
### while and do Loops
```
let number = 0; 
while (number <= 12) { 
	console.log(number); number = number + 2; 
} 
// → 0
// → 2 
// ... etcetera
```
### Indenting Code
```
if (false != true) {
	console.log("That makes sense."); 
	if (1 < 2) { 
		console.log("No surprise there.");
	} 
}
```
### for Loops
```
for (let number = 0; number <= 12; number = number + 2) { 
	console.log(number); 
} 
// → 0 
// → 2 
// ... etcetera
```
### Breaking Out of a Loop
```
for (let current = 20; ; current = current + 1) {
	if (current % 7 == 0) {
	console.log(current); break; 
	} 
} 
// → 21
```
### Updating Bindings Succinctly
### Dispatching on a Value with switch
```
switch (prompt("What is the weather like?")) {
	case "rainy":
		console.log("Remember to bring an umbrella."); 
		break;
	case "sunny":
		console.log("Dress lightly.");
	case "cloudy":
		console.log("Go outside.");
		break;
	default:
	console.log("Unknown weather type!");
	break;
}
```
### Capitalization
```
fuzzylittleturtle
fuzzy_little_turtle
FuzzyLittleTurtle
fuzzyLittleTurtle
```
### Comments
```
let accountBalance = calculateBalance(account);
// It's a green hollow where a river sings
accountBalance.adjust();
// Madly catching white tatters in the grass.
let report = new Report();
// Where the sun on the proud mountain rings:
addToReport(accountBalance, report);
// It's a little valley, foaming like light in a glass.
```