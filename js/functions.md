# Functions

> A JavaScript function is a block of code designed to perform a particular task.
A JavaScript function is executed when "something" invokes it (calls it).
> 
> Functions in Javascript are the main building blocks of the program. They allow code to be called many times without repetition.

---

## Syntax
A JavaScript function is defined with the function keyword, followed by a name, followed by parentheses ().

Function names can contain letters, digits, underscores, and dollar signs (same rules as variables).

The parentheses may include parameter names separated by commas:
(parameter1, parameter2, ...)

The code to be executed, by the function, is placed inside curly brackets: {}

```js
function name(parameter1, parameter2, parameter3) {
  // code to be executed
}
```

Function parameters are listed inside the parentheses () in the function definition.

Function arguments are the values received by the function when it is invoked.

Inside the function, the arguments (the parameters) behave as local variables.

---

## Invoking Functions

To use function after it has been defined, you've got to run — or invoke — it. This is done by including the name of the function in the code somewhere, followed by parentheses.

```js
function myFunction() {
  alert('hello');
}

myFunction();
// calls the function once
```
---

## Function Declaration

> To create a function, we can use a function declaration.

```js
function showMessage() {
  alert( 'Hello everyone!' );
}
```

---
## Function expressions
>There is another syntax for creating a function that is called a Function Expression.
It allows us to create a new function in the middle of any expression.

```js
let sayHi = function() {
  alert( "Hello" );
};
```

A Function Expression is created when the execution reaches it and is usable only from that moment.

Once the execution flow passes to the right side of the assignment let sum = function… – here we go, the function is created and can be used (assigned, called, etc. ) from now on.

Function Declarations are different.

A Function Declaration can be called earlier than it is defined.

---

## Local Variables/scope
>A variable declared inside a function is only visible inside that function.

```js
function showMessage() {
  let message = "Hello, I'm JavaScript!"; // local variable

  alert( message );
}

showMessage(); // Hello, I'm JavaScript!

alert( message ); // <-- Error! The variable is local to the function
```

### Global Variables/scope
>Values defined in the global scope are accessible from everywhere in the code.

```js
let userName = 'John';

function showMessage() {
  let userName = "Bob"; // declare a local variable

  let message = 'Hello, ' + userName; // Bob
  alert(message);
}

// the function will create and use its own userName
showMessage();

alert( userName ); // John, unchanged, the function did not access the outer variable
```

## Arrow Functions
>Arrow functions allow us to write shorter function syntax.

```js
// function expression
let x = function(x, y) {
   return x * y;
}

can be written as

// using arrow functions
let x = (x, y) => x * y;