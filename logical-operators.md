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
> The  `&&(AND)` operator  uses double ampersand (`&&`) to represent this logical operator.

```js
let result = a && b;
```

If a can be converted to true, the && operator returns the b; otherwise, it returns the a. In fact, this rule is applied to all boolean values.

There are four possible logical combinations: 
```js
alert( true && true );   // true
alert( false && true );  // false
alert( true && false );  // false
alert( false && false ); // false
```

### AND `&&` finds the first falsy value
Evaluates operands from left to right.
For each operand, converts it to a boolean. If the result is false, stops and returns the original value of that operand.
If all operands have been evaluated (i.e. all were truthy), returns the last operand.<br>
In other words, AND returns the first falsy value or the last value if none were found.

```js
// if the first operand is truthy,
// AND returns the second operand:
alert( 1 && 0 ); // 0
alert( 1 && 5 ); // 5

// if the first operand is falsy,
// AND returns it. The second operand is ignored
alert( null && 5 ); // null
alert( 0 && "no matter what" ); // 0
```

Some examples of `AND(&&)` with an `if statement`

```js
let hour = 12;
let minute = 30;

if (hour == 12 && minute == 30) {
  alert( 'The time is 12:30' );
}
```
```js
if (1 && 0) { // evaluated as true && false
  alert( "won't work, because the result is falsy" );
}
```
---
> ## Don't replace `if` with `||` or `&&`.


Sometimes, people use the AND && operator as a "shorter way to write if".

For instance:

```js
let x = 1;

(x > 0) && alert( 'Greater than zero!' );
```
The action in the right part of && would execute only if the evaluation reaches it. That is, only if (x > 0) is true.

So we basically have an analogue for:
```js
let x = 1;

if (x > 0) alert( 'Greater than zero!' );
```
Although, the variant with && appears shorter, if is more obvious and tends to be a little bit more readable. So we recommend using every construct for its purpose: use if if we want if and use && if we want AND.

---

## `!` (NOT)

>The `!`(NOT) operator uses an exclamation mark (!) to represent the logical NOT operator. The ! operator can be applied to a single value of any type, not just a Boolean value.

```js
result = !value;
```
The operator converts the operand to a boolean type (true/false) then returns the inverse value.
```js
alert( !true ); // false
alert( !0 ); // true
```
A double NOT !! is sometimes used for converting a value to boolean type:
```js
alert( !!"non-empty string" ); // true
alert( !!null ); // false
That is, the first NOT converts the value to boolean and returns the inverse, and the second NOT inverses it again. 
```
---

## Operator Precedence

## `!` > `&&` > `||`
---