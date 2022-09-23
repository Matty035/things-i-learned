# Numbers 

## Types of Numbers

> - **Intergers** are floating-point numbers without a fraction, either postive or negative, e.g. 5, 60, -700  
> - **Floating point numbers** (floats) have decimal points and decimal places, e.g. 12.5, and 56.7786543.
> -  **Doubles** are a specific type of floating point number that have greater precision than standard floating point numbers (meaning that they are accurate to a greater number of decimal places).

---
### Adding Numbers and Strings

>JavaScript uses the + operator for both addition and concatenation.
Numbers are added. Strings are concatenated.

**If you add two numbers, the result will be a number.**

**If you add two string, the result will be a string concatenation.**

**If you add a number and a string, the result will be a string concatenation**

---

### The Number() Method
>`Number()` can be used to convert JavaScript variables to numbers:

```js
Number(true);
Number(false);
Number("10");
Number("  10");
Number("10  ");
Number(" 10  ");
Number("10.33")
```

### NaN - Not a Number

>NaN is a JavaScript reserved word indicating that a number is not a legal number.<br>
Trying to do arithmetic with a non-numeric string will result in NaN (Not a Number).<br>
**NaN is a number: `typeof` NaN returns number**



```js
  let x = 100 / "Apple";   x = `NaN`
```
**However, if the string contains a numeric value , the result will be a number**

**You can use the global JavaScript function isNaN() to find out if a value is a not a number:**

```js
let x = 100 / "Apple";
isNaN(x);
```
**Watch out for NaN. If you use NaN in a mathematical operation, the result will also be NaN**






