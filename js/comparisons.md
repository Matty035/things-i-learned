# Comparisons

> Comparisons are used to test for `true` or `false`. <br>
>  All comparison operators return a boolean value. <br>eg. `True` - means yes, correct or the truth. `False` - means no, wrong, or not the truth

```js
alert( 2 > 1 );  // true (correct)
alert( 2 == 1 ); // false (wrong)
alert( 2 != 1 ); // true (correct)
```

A comparison result can be assigned to a variable, just like any value:
```js
let result = 5 > 4; // assign the result of the comparison
alert( result ); // true
```
---
## Comparison Operators

>To do these tests we use comparison operators to determine the difference between variables or values.

| Operator | Name | Purpose | Example | 
| :---: | :---: | :---: | :--- |
`===` | Strict equality (True)| Tests whether the left and right values are identical to one another | ` 5 === 2 + 4 ` |
` !== ` | Strict-non-equality  (False) | Tests whether the left and right values are not identical to one another | ` 5 !==2 + 3 ` |
` < ` | Less than | Tests whether the left value is smaller than the right one | ` 10 < 6 ` |
` > ` | Greater than | Tests whether the left value is greater than the right one | ` 10 > 20 ` |
` <= ` |  Less than or equal to | Tests whether the left value is smaller than or equal to the right one | `3 <= 2` |  
`>=` | Greater than or equal to | Tests whether the left value is greater than or equal to the right one | `4 >= 3 `|
---
## Comparison of diferent types

> When comparing values of different types, javascript will convert the values to numbers.

```js
alert( '2' > 1 ); // true, string '2' becomes a number 2
alert( '01' == 1 ); // true, string '01' becomes a number 1
```
---
## String comparison
>To see whether a string is greater than another, JavaScript uses the so-called “dictionary” or “lexicographical” order. Put simply, the stings are compared letter by letter.

```js
alert( 'Z' > 'A' ); // true
alert( 'Glow' > 'Glee' ); // true
alert( 'Bee' > 'Be' ); // true
```
