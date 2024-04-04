### Unary
An operator is unary if it has a single operand. For example, the unary negation - reverses the sign of a number:

```javascript
let x = 1;

x = -x;
alert( x ); // -1, unary negation was applied

```

### Maths Operations
- Addition +
- Subtraction
- Multiplication
- Division
- Remainder %
- Exponentation **
---
### Exponentation
The exponentiation operator a ** b raises a to the power of b.


``` javascript
alert( 2 ** 2 ); // 2² = 4
alert( 2 ** 3 ); // 2³ = 8
alert( 2 ** 4 ); // 2⁴ = 16

```

---
### Binary + operator in JS
JavaScript's binary `+` operator concatenates strings when applied to string operands. If either operand is a string, the other is converted to a string as well. For instance:

- `let s = "my" + "string";` results in `"mystring"`.
- `alert('1' + 2);` yields `"12"`.
- `alert(2 + '1');` yields `"21"`.
- The order of operands doesn't matter.

In complex expressions:

- `alert(2 + 2 + '1');` evaluates to `"41"`.
- `alert('1' + 2 + 2);` evaluates to `"122"`.

---
 
 ### unary `+` as  numeric converter
 The plus + exists in two forms: the binary form that we used above and the unary form.

The unary plus or, in other words, the plus operator + applied to a single value, doesn’t do anything to numbers. But if the operand is not a number, the unary plus converts it into a number.

For example:

```javascript
let x = 1;
alert( +x ); // 1

let y = -2;
alert( +y ); // -2

// Converts non-numbers
alert( +true ); // 1
alert( +"" );   // 0
```

> unary + does the same work as Number(....)

Example 1:
```js
let apples = "2";
let oranges = "3";

alert( apples + oranges ); // "23", the binary plus concatenates strings
```

Example 2:
```js
let apples = "2";
let oranges = "3";

// both values converted to numbers before the binary plus
alert( +apples + +oranges ); // 5

// the longer variant
// alert( Number(apples) + Number(oranges) ); // 5
```

---
### Chaining Assignments operator
```Js
let a, b, c;

a = b = c = 2 + 2;

alert( a ); // 4
alert( b ); // 4
alert( c ); // 4
```

---
### Bitwise Operator
treats arguments as 32-bit integer and work on binary level.
- AND ( & ) 
- OR ( | )
- XOR ( ^ )
- NOT ( ~ )
- LEFT SHIFT ( << )
- RIGHT SHIFT ( >> )
- ZERO-FILL RIGHT SHIFT ( >>> )

used rarely.

---
### Comma Operator
rarest and unusal operator
```js
let a = (1 + 2, 3 + 4);

alert( a ); // 7 (the result of 3 + 4)
```
Tallows us to evaluate several expressions, dividing them with a comma ,. 
<br> Each of them is evaluated but only the result of the last one is returned.

---
## Exercise

What are results of these expressions?
```js
"" + 1 + 0
"" - 1 + 0
true + false
6 / "3"
"2" * "3"
4 + 5 + "px"
"$" + 4 + 5
"4" - 2
"4px" - 2
"  -9  " + 5
"  -9  " - 5
null + 1
undefined + 1
" \t \n" - 2
```
---
### Answer
```js
"" + 1 + 0 = "10" // The addition with a string "" + 1 converts 1 to a string: "" + 1 = "1", and then we have "1" + 0, the same rule is applied.

"" - 1 + 0 = -1 // The subtraction - (like most math operations) only works with numbers, it converts an empty string "" to 0.
true + false = 1 
6 / "3" = 2
"2" * "3" = 6
4 + 5 + "px" = "9px"
"$" + 4 + 5 = "$45"
"4" - 2 = 2
"4px" - 2 = NaN
"  -9  " + 5 = "  -9  5" // The addition with a string appends the number 5 to the string.
"  -9  " - 5 = -14 // The subtraction always converts to numbers, so it makes " -9 " a number -9 (ignoring spaces around it).
null + 1 = 1 // null becomes 0 after the numeric conversion.
undefined + 1 = NaN // undefined becomes NaN after the numeric conversion.
" \t \n" - 2 = -2 // Space characters are trimmed off string start and end when a string is converted to a number. Here the whole string consists of space characters, such as \t, \n and a “regular” space between them. So, similarly to an empty string, it becomes 0.

```
