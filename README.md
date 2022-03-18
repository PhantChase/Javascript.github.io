# PART I
## MODULES
### Modules as Building Blocks
### Improvised Modules
```
const weekDay = function() {
	const names = ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"];
return {
	name(number) { return names[number]; },
	number(name) { return names.indexOf(name); }
};
}();
console.log(weekDay.name(weekDay.number("Sunday")));
// → Sunday
```
### Evaluating Data as Code
```
const x = 1; function evalAndReturnX(code) {
	eval(code);
	return x;
}
console.log(evalAndReturnX("var x = 2"));
// → 2
console.log(x);
// → 1
```
### CommonJS
```
const {parse} = require("ini");
console.log(parse("x = 10\ny = 20"));
// → {x: "10", y: "20"}
```
### ECMAScript Modules
```
import {days as dayNames} from "date-names";
console.log(dayNames.length);
// → 7
```