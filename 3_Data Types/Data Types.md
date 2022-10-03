# Overview
- [Data Types](#data-types)
  - [Primitive Types](#primitive-types)
    - [String](#string)
    - [Boolean](#boolean)
    - [Number](#number)
    - [Undefined](#undefined)
    - [Symbol](#symbol)
    - [#Bihint](#bigint)
  - [Non-Primitive Type](#non-primitive-type)
  - [Object](#object)

# **Data Types**
In JavaScript and also other programming languages, there are different types of data types. The following are JavaScript primitive data types: _String, Number, Boolean, undefined, Null_, and _Symbol_.
We can put any type in a variable. For example, a variable can at one moment be a string and then store a number:
```js
// no error
let message = "hello";
message = 123456;
```
Programming languages that allow such things, such as JavaScript, are called “dynamically typed”, meaning that there exist data types, but variables are not bound to any of them.

There are two Types:
  - Primitive
  - Non-Primitive


# Primitive Types
In JavaScript, a primitive (primitive value, primitive data type) is data that is not an object and has no methods or properties.
## String
A string in JavaScript must be surrounded by quotes.
```js
let str = "Hello";
let str2 = 'Single quotes are ok too';
let phrase = `can embed another ${str}`;
```
In JavaScript, there are 3 types of quotes.

- Double quotes: "Hello".
- Single quotes: 'Hello'.
- Backticks: `Hello`.
Double and single quotes are “simple” quotes. There’s practically no difference between them in JavaScript.

Backticks are “extended functionality” quotes. They allow us to embed variables and expressions into a string by wrapping them in `${…}`, for example:  
```js
let name = "John";

// embed a variable
alert( `Hello, ${name}!` ); // Hello, John!

// embed an expression
alert( `the result is ${1 + 2}` ); // the result is 3
```
The expression inside `${…}` is evaluated and the result becomes a part of the string. We can put anything in there: a variable like `name` or an arithmetical expression like `1 + 2` or something more complex.

Please note that this can only be done in backticks. Other quotes don’t have this embedding functionality!



## Number
## Boolean
## Undefined
## Null
## Symbol
## Bigint
In JavaScript, the “number” type cannot safely represent integer values larger than `(2^53-1)` (that’s `9007199254740991`), or less than `-(2^53-1)` for negatives.

To be really precise, the “number” type can store larger integers (up to `1.7976931348623157 * 10308`), but outside of the safe integer range `±(2^53-1)` there’ll be a precision error, because not all digits fit into the fixed 64-bit storage. So an “approximate” value may be stored.

For example, these two numbers (right above the safe range) are the same:
```js
console.log(9007199254740991 + 1); // 9007199254740992
console.log(9007199254740991 + 2); // 9007199254740992
```
So to say, all odd integers greater than `(2^53-1)` can’t be stored at all in the “number” type.

For most purposes `±(2^53-1)` range is quite enough, but sometimes we need the entire range of really big integers, e.g. for cryptography or microsecond-precision timestamps.
You can check Following [BigInt compatibility table](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/BigInt#browser_compatibility) to know which versions of a browser are supported.

![Compatibility Table](/images/Compatibality_Table.png)


`BigInt` type was recently added to the language to represent integers of arbitrary length.

A `BigInt` value is created by appending n to the end of an integer:
```js
// the "n" at the end means it's a BigInt
const bigInt = 1234567890123456789012345678901234567890n;
```
As `BigInt` numbers are rarely needed, we don’t cover them here, but devoted them a separate chapter BigInt. Read it when you need such big numbers.


# Non-Primitive Type
These Types contain Objects, have properties and have some methods to them 

# Object
JavaScript object is a data structure that allows us to have key-value pairs; so we can have distinct keys and each key is mapped to a value that can be of any JavaScript data type. Comparing it to a real-world object, a pen is an object with several properties such as color, design, the material it is made of, etc. In the same way, JavaScript objects can have properties that define their characteristics.
##  object.freeze()