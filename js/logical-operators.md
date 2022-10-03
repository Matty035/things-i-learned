# Logical Operators
> There are four logical operators in JavaScript: `||` (OR) `&&` (AND) `!` (NOT) `??`(Nullish Coalescing) <br>
> They can be applied to values of any type, and their result can be also of any type.

## `||` (OR)
>JavaScript uses the double pipe `||` to represent the logical OR operator. You can apply the `||` operator to two values of any type:

```js
result = a || b;
```
If a can be converted to true, returns a; else, returns b. This rule is also applied to boolean values.

There are four possible logical combinations:
```js
alert( true || true );   // true
alert( false || true );  // true
alert( true || false );  // true
alert( false || false ); // false
```
### OR finds the first truthy value.

The OR || operator does the following:

Evaluates operands from left to right.
For each operand, converts it to boolean. If the result is true, stops and returns the original value of that operand.
If all operands have been evaluated (i.e. all were false), returns the last operand.
A value is returned in its original form, without the conversion.

In other words, a chain of OR || returns the first truthy value or the last one if no truthy value is found.

```js alert( 1 || 0 ); // 1 (1 is truthy)
alert( null || 1 ); // 1 (1 is the first truthy value)
alert( null || 0 || 1 ); // 1 (the first truthy value)

alert( undefined || null || 0 ); // 0 (all falsy, returns the last value)
```
Some examples of using OR `||` in an `if statement`:

```js
let hour = 9;

if (hour < 10 || hour > 18) {
  alert( 'The office is closed.' );
}
```
We can pass more conditions:
```js
let hour = 12;
let isWeekend = true;

if (hour < 10 || hour > 18 || isWeekend) {
  alert( 'The office is closed.' ); // it is the weekend
}
```
---
## `&& (AND)`
> The  `&&(AND)` operator  