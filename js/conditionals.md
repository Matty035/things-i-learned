# Conditionals
> Conditional statements are used to perform different actions based on different conditions.

In JavaScript we have the following conditional statements:

>Use `if` to specify a block of code to be executed, if a specified condition is true <br>
Use `else` to specify a block of code to be executed, if the same condition is false<br>
Use `else if` to specify a new condition to test, if the first condition is false<br>
Use `switch` to specify many alternative blocks of code to be executed

Basic syntax

```js
if (condition) {
  /* code to run if condition is true */
} else {
  /* run some other code instead */
}
```

## The if Statement.
>The if(...) statement evaluates a condition in parentheses and, if the result is true, executes a block of code.<br>
The if (…) statement evaluates the expression in its parentheses and converts the result to a boolean.


```js
let year = (2015);

if (year == 2015) alert( 'You are right!' );
```
If we want to execute more than one statement, we have to wrap our code block inside curly braces:
```js
if (year == 2015) {
  alert( "That's correct!" );
  alert( "You're so smart!" );
}
```
---
## The else statement.
>Use the `else` statement to specify a block of code to be executed if the condition is false.
```js
let year = 2015;

if (year == 2015) {
  alert( 'You guessed it right!' );
} else {
  alert( 'How can you be so wrong?' ); // any value except 2015
}
```
---
## The else if statement.
> The else if statement is used to if we want more than two outcomes/choices.

```js
let year = 2015;

if (year < 2015) {
  alert( 'Too early...' );
} else if (year > 2015) {
  alert( 'Too late' );
} else {
  alert( 'Exactly!' );
}
```
In the code above, JavaScript first checks year < 2015. If that is falsy, it goes to the next condition year > 2015. If that is also falsy, it shows the last alert.
There can be more else if blocks. The final else is optional.

---

## The switch statement.
>The switch statement is used to perform different actions based on different conditions. <br>
You use the switch statement to select on of the many code blocks to be executed.

### Syntax

```js
switch(expression) {
  case x:
    // code block
    break;
  case y:
    // code block
    break;
  default:
    // code block
}
```
This is how it works:

The switch expression is evaluated once.
The value of the expression is compared with the values of each case.
If there is a match, the associated block of code is executed.
If there is no match, the default code block is executed.

example :
```js
let a = 2 + 2;

switch (a) {
  case 3:
    alert( 'Too small' );
    break;
  case 4:
    alert( 'Exactly!' );
    break;
  case 5:
    alert( 'Too big' );
    break;
  default:
    alert( "I don't know such values" );
}
```

### Grouping of `case`
Several variants of case which share the same code can be grouped.<br>
For example, if we want the same code to run for case 3 and case 5:

```js
let a = 3;

switch (a) {
  case 4:
    alert('Right!');
    break;

  case 3: // (*) grouped two cases
  case 5:
    alert('Wrong!');
    alert("Why don't you take a math class?");
    break;

  default:
    alert('The result is strange. Really.');
}
```
Now both 3 and 5 show the same message.<br>
The ability to “group” cases is a side effect of how switch/case works without break. Here the execution of case 3 starts from the line (*) and goes through case 5, because there’s no break.

### Type Matters
Let’s emphasize that the equality check is always strict. The values must be of the same type to match.

```js
let arg = prompt("Enter a value?");
switch (arg) {
  case '0':
  case '1':
    alert( 'One or zero' );
    break;

  case '2':
    alert( 'Two' );
    break;

  case 3:
    alert( 'Never executes!' );
    break;
  default:
    alert( 'An unknown value' );
}
```
For 0, 1, the first alert runs.<br>
For 2 the second alert runs.<br>
But for 3, the result of the prompt is a string "3", which is not strictly equal === to the number 3. So we’ve got a dead code in case 3! The default variant will execute.

---

## Ternary Operator/ Conditional Operator

>The operator is represented by a question mark ?. Sometimes it’s called “ternary”, because the operator has three operands. It is actually the one and only operator in JavaScript which has that many.

### Syntax

```js
let result = condition ? value1 : value2;
```
The condition is evaluated: if it’s truthy then value1 is returned, otherwise – value2.

#### Example
```js
let accessAllowed = (age > 18) ? true : false;
```
### Multiple ?
>A sequence of question mark operators ? can return a value that depends on more than one condition.

#### Example
```js
let age = prompt('age?', 18);

let message = (age < 3) ? 'Hi, baby!' :
  (age < 18) ? 'Hello!' :
  (age < 100) ? 'Greetings!' :
  'What an unusual age!';

alert( message );
```

The first question mark checks whether age < 3.<br>
If true – it returns 'Hi, baby!'. Otherwise, it continues to the expression after the colon ‘":"’, checking age < 18.<br>
If that’s true – it returns 'Hello!'. Otherwise, it continues to the expression after the next colon ‘":"’, checking age < 100. <br>
If that’s true – it returns 'Greetings!'. Otherwise, it continues to the expression after the last colon ‘":"’, returning 'What an unusual age!'.

