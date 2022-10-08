# Data Types

> A value in Javascript is always of a certain type. 

Seven primitive data types:<br>
`Number` for numbers of any kind: integer or floating-point, integers are limited by ±(253-1). <br>
`Bigint` for integer numbers of arbitrary length. <br>
`String` for strings. A string may have zero or more characters, there’s no separate single-character type. <br>
`Boolean` for true/false. <br>
`Null` for unknown values – a standalone type that has a single value null. <br>
`Undefined` for unassigned values – a standalone type that has a single value undefined.

And one non-primitive data type: <br>
`Object` for more complex data structures.

The `Type of` operator allows us to see which type is stored in a variable.

Usually used as typeof x, but typeof(x) is also possible.<br>
Returns a string with the name of the type, like "string".<br>
For null returns "object" – this is an error in the language, it’s not actually an object.
