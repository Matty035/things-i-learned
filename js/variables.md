# **Variables**

>A variable is a storage container for data in your code.
There is 3 ways to create a variable:

- `let`
- `var`
- `const`

## **A variable**
```js
let message; 
message = 'Hello'; /
store the string 'Hello' in the variable named message
```
There are a number of different ways to declare variables.

**Singleline variant**
```js
let user = 'John', age = 25, message = 'Hello';
```


**Multiline variant**
```js
let user = 'John';
let age = 25;
let message = 'Hello';
```
**Another way to do multiline**
```js
let user = 'John',
  age = 25,
  message = 'Hello';
  ```

#### **Variable Naming**

There are two limitations on variable names in javascript.

1.The name must only contain letters,digits or `$` and `_` symbols.

2.The first character must not be a digit.

Examples of valid names:

```js
let userName;
let test123;
```
When the name contains multiple words, camelCase is commonly used. That is: words go one after another, each word except first starting with a capital letter: myVeryLongName.

>**Case Matter**  
Variables named orange and ORANGE are two different variables.







### **var instead of let**
The var keyword is almost the same as 'let', it also declares a variable but in an old school way. 


---

## Constants

>To declare a constant(unchanging) variable use `const` instead of `let`.

  ```js
  const myBirthday = '18.04.1982';
  ```

Variables declared using 'const' cannot be reassigned, attemping to do so would cause an error

### Uppercase constants

>There is a widespread practice to use constants as aliases for difficult-to-remember values that are known prior to execution.

```js
const COLOR_RED = "#F000"
const COLOR_GREEN ="#0F0" 
const COLOR_BLUE = "#00F";  
const COLOR_ORANGE ="#FF7F00";

// ...when we need to pick a color  
let color = COLOR_ORANGE;  
alert(color); // #FF7F00
```

