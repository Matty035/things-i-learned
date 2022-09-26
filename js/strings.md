# Strings

>Strings are for storing and manipulating text in JavaScript.<br>A JavaScript string is zero or more characters written inside quotes.

---
**You can either use single `' '` or double `" "` quotiation marks.**

```js
const sgl = 'Single quotes.';
const dbl = "Double quotes";
console.log(sgl);
console.log(dbl);
```

### Template literal 
A template literal looks just like a normal string, but instead of using single or double quote marks (' or "), you use backtick characters ` `` `:

```js
const greeting = `Hello`;
```

This can work just like a normal string, except you can include variables in it, wrapped inside ${ } characters, and the variable's value will be inserted into the result:

```js
const name = 'Chris';
const greeting = `Hello, ${name}`;
console.log(greeting); // "Hello, Chris"
```

You can use the same technique to join together two variables:

```js
const one = 'Hello, ';
const two = 'how are you?';
const joined = `${one}${two}`;
console.log(joined); // "Hello, how are you?"
```
You can also concatenate strong by using the `+` operator.

```js
const greeting = "Hello";
const name = "Chris";
console.log(greeting + ", " + name); // "Hello, Chris"
```

## Numbers vs Strings

> To convert a number to a string we can use the `toString()` method.

```js
const myNum2 = 123;
const myString2 = myNum2.toString();
console.log(typeof myString2);
```

>Or if we want to change a string to a number we can use the `number` object.

```js
const myString = '123';
const myNum = Number(myString);
console.log(typeof myNum);
```

There are a number of String methods available to use in JavaScript. 
Here is a think to them.
[String Methods](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Useful_string_methods)