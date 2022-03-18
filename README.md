# PART I
## REGULAR EXPRESSIONS
### Creating a Regular Expression
```
let re1 = new RegExp("abc");
let re2 = /abc/;
```
### Testing for Matches
```
console.log(/abc/.test("abcde"));
// → true
console.log(/abc/.test("abxde"));
// → false
```
### Sets of Characters
```
let notBinary = /[^01]/;
console.log(notBinary.test("1100100010100110")); // → false
console.log(notBinary.test("1100100010200110")); // → true
```
### Repeating Parts of a Pattern
```
let neighbor = /neighbou?r/;\
console.log(neighbor.test("neighbour")); // → true
console.log(neighbor.test("neighbor")); // → true
```
### Grouping Subexpressions
```
let cartoonCrying = /boo+(hoo+)+/i;
console.log(cartoonCrying.test("Boohoooohoohooo")); // → true
```
### Matches and Groups
```
console.log(/bad(ly)?/.exec("bad"));
// → ["bad", undefined]
console.log(/(\d)+/.exec("123"));
// → ["123", "3"]
```
### The Date Class
```
function getDate(string) {
	let [_, month, day, year] = /(\d{1,2
})-(
\d{1,2})-(\d{4})/.exec(string);
	return new Date(year, month - 1, day);
}
console.log(getDate("1-30-2003"));
// → Thu Jan 30 2003 00:00:00 GMT+0100 (CET)
```
### Word and String Boundaries
### Choice Patterns
```
let animalCount = /\b\d+ (pig|cow|chicken)s?\b/;
console.log(animalCount.test("15 pigs"));
// → true
console.log(animalCount.test("15 pigchickens"));
// → false
```
### The Mechanics of Matching
### Backtracking
### The replace Method