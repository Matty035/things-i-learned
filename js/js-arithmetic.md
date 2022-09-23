# Javascript Arithmetic


## Operators and Operands


>The numbers (in an arithmetic operation) are called operands.  
>The operation (to be performed between the two operands) is defined by an operator.

###  Arithmetic Operators


 | Operator | Name | Purpose | Example |
 | :---: | :---: | :---: | :---: |
 | `+ `| Addition| Adds two numbers together | `2 + 2`
 |`- `| Subtraction | Subracts two numbers | `15 - 7`|
 | `*` | Multiplication | Multiplies tow numbers together | `5 * 5` |
 | `**` | Exponentiation (Power) | Operation of raising one quanity to power of another | `5 ** 2` (returns 25, which is the same as 5 * 5).
 | `/` | Division | Divides left number by the right | `10 / 5` |
 |` %` | Modulus (Remainder) | the remainder when one integer is divided by another | `7 % 3` (returns 2 with 1 left remainding)
 | `++` | Increment | Increments numbers | `2++ = 3` |
 | `--` | Decrement | Decrements Numbers | `4-- = 3` |

---

## Assignment Operators

>Assignment operators are operators that assign a value to a variable. We have already used the most basic one, =, loads of times — it assigns the variable on the left the value stated on the right:

```js
let x = 3; // x contains the value 3
let y = 4; // y contains the value 4
x = y; // x now contains the same value y contains, 4
```

| Operator | Name | Purpose | Example | Shortcut for |
| :---: | :---: | :---: | :---: | :---: |
|`+=`| Addition <br> Assignment | Adds the value on the right to the variable value on the left, <br> then returns the new variable value | ` x += 4` | `x = x + 4`|
`-=` | Subtraction <br> Assignment | Subtracts the value on the right from the variable value on the left, <br> and returns the new variable value | ` x -= 3` | ` x = x - 3 ` |
` *= ` | Multiplication <br> Assignment | Multiplies the variable value on the left by the value on the right, <br> and returns the new variable value | ` x *= 3` | `x = x * 3 ` |
` /= `| Division <br> Assignment | Divides the variable value on the left by the value on the right,<br> and returns the new variable value | ` x /= 4` | ` x = x / 4 ` |

```js
let x = 3; // x contains the value 3
let y = 4; // y contains the value 4
x *= y; // x now contains the value 12
```
---

## Comparison Operators

>Sometimes we will want to run true/false tests, then act accordingly depending on the result of that test — to do this we use comparison operators.

| Operator | Name | Purpose | Example | 
| :---: | :---: | :---: | :--- |
`===` | Strict equality (True)| Tests whether the left and right values are identical to one another | ` 5 === 2 + 4 ` |
` !== ` | Strict-non-equality  (False) | Tests whether the left and right values are not identical to one another | ` 5 !==2 + 3 ` |
` < ` | Less than | Tests whether the left value is smaller than the right one | ` 10 < 6 ` |
` > ` | Greater than | Tests whether the left value is greater than the right one | ` 10 > 20 ` |
` <= ` |  Less than or equal to | Tests whether the left value is smaller than or equal to the right one | `3 <= 2` |  
`>=` | Greater than or equal to | Tests whether the left value is greater than or equal to the right one | `4 >= 3 `|









