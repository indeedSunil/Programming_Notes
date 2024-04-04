### String Comparision
```js

console.log('Z' > 'A') //true
console.log('glow' > 'glee') //true
```
String comparision is checked letter by letter like in a dictionary
<br>
Actually , it is done by unicode order which is roughly equivalent to the one used in dictionary but it's not exactly the same.

  *for example: a is greater than A*
  <br>
  *Why? Because the lowercase character has a greater index in the internal encoding table JavaScript uses (Unicode)*


 ### A funny consequence
It is possible that at the same time:

Two values are equal. 
<br>
One of them is true as a boolean and the other one is false as a boolean.
For example:
```js
let a = 0;
alert( Boolean(a) ); // false

let b = "0";
alert( Boolean(b) ); // true

alert(a == b); // true!
```
From JavaScript’s standpoint, this result is quite normal. An equality check converts values using the numeric conversion (hence "0" becomes 0), while the explicit Boolean conversion uses another set of rules.

---
### The `===` operator
`===` is used for strict checking in JS.
This compares the value and datatypes and return true only when both of them are equal.

- null == undefined  `true`
- null === undefined `false`
  
---
### Something Fun
```js
alert( null > 0 );  // (1) false
alert( null == 0 ); // (2) false
alert( null >= 0 ); // (3) true
```

Mathematically it's strange but the reason behind this is that: <br>
>Comparision operators convert null to a number treating it as 0 while equality check does that wihtout converting.

*undefined always returns false in any case*

---
### Summary
- Comparison operators return a boolean value.
- Strings are compared letter-by-letter in the “dictionary” order.
- When values of different types are compared, they get converted to numbers (with the exclusion of a strict equality check).
- The values null and undefined equal == each other and do not equal any other value.
- Be careful when using comparisons like > or < with variables that can occasionally be null/undefined. Checking for null/undefined separately is a good idea.