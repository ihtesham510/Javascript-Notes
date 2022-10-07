
## Overview

- [Variables](#variables)
  - [Naming Rules](#naming-rules)
  - [Hoisting](#hoisting)
  - [Variable Declaration]()
    - [var](#var)
    - [const](#const)
    - [let](#let)
  - [Variables Scopes](#variables-scopes)
    - [Block Scopes](#block-scope)
    - [Local Scopes](#local-scope)
    - [Functional Scopes](#functional-scope)
    - [Global Scopes](#global-scope)


      
# ***Variables***

Variables are containers for storing data (storing data values).

In this example, x, y, and z, are variables, declared with the var keyword:
```js
var x = 5;
var y = 6;
var z = x + y;
```
## ***The Assignment Operator***

In JavaScript, the equal sign (=) is an "assignment" operator, not an "equal to" operator.

This is different from algebra. The following does not make sense in algebra:
```js
x = x + 5
```
In JavaScript, however, it makes perfect sense: it assigns the value of x + 5 to x.

(It calculates the value of x + 5 and puts the result into x. The value of x is incremented by 5.)


**Note**

The "equal to" operator is written like == in JavaScript.
## ***Diffrence Between Primitive and Non-Primitive Types***
Now, let us see what exactly primitive and non-primitive data types mean.

</d>

*Primitive* data types are immutable(non-modifiable) data types. Once a primitive data type is created we cannot modify it.

**Example:**

```js
let word = 'JavaScript'
```

If we try to modify the string stored in variable *word*, JavaScript should raise an error. Any data type under a single quote, double quote, or backtick quote is a string data type.

```js
word[0] = 'Y'
```

This expression does not change the string stored in the variable *word*. So, we can say that strings are not modifiable or in other words immutable.
Primitive data types are compared by its values. Let us compare different data values. See the example below:

```js
let numOne = 3
let numTwo = 3

console.log(numOne == numTwo)      // true

let js = 'JavaScript'
let py = 'Python'

console.log(js == py)             //false 

let lightOn = true
let lightOff = false

console.log(lightOn == lightOff) // false
```
*Non-primitive* data types are modifiable or mutable. We can modify the value of non-primitive data types after it gets created.
Let us see by creating an array. An array is a list of data values in a square bracket. Arrays can contain the same or different data types. Array values are referenced by their index. In JavaScript array index starts at zero. I.e., the first element of an array is found at index zero, the second element at index one, and the third element at index two, etc.

```js
let nums = [1, 2, 3]
nums[0] = 10

console.log(nums)  // [10, 2, 3]
```

As you can see, an array, which is a non-primitive data type is mutable. Non-primitive data types cannot be compared by value. Even if two non-primitive data types have the same properties and values, they are not strictly equal.

```js
let nums = [1, 2, 3]
let numbers = [1, 2, 3]

console.log(nums == numbers)  // false

let userOne = {
name:'Asabeneh',
role:'teaching',
country:'Finland'
}

let userTwo = {
name:'Asabeneh',
role:'teaching',
country:'Finland'
}

console.log(userOne == userTwo) // false
```

Rule of thumb, we do not compare non-primitive data types. Do not compare arrays, functions, or objects.
Non-primitive values are referred to as reference types, because they are being compared by reference instead of value. Two objects are only strictly equal if they refer to the same underlying object.

```js
let nums = [1, 2, 3]
let numbers = nums

console.log(nums == numbers)  // true

let userOne = {
name:'Asabeneh',
role:'teaching',
country:'Finland'
}

let userTwo = userOne

console.log(userOne == userTwo)  // true
```

If you have a hard time understanding the difference between primitive data types and non-primitive data types, you are not the only one. Calm down and just go to the next section and try to come back after some time. Now let us start the data types by number type.



# Naming Rules

 1. Cannot be a reserved keyword.
 2. Should be meaningfull. 
      - Use Names(like : Interest_Rate) instead of Letters like (x,y,z).
      - This can prevent us having bugs in our projects.
 3. Variables cannot start with a number (1name).
 4. Cannot contain a space or a hyphen(-).
 5. Varialbles are Case-Sensitive.

# Hoisting
JavaScript Hoisting refers to the process whereby the interpreter appears to move the declaration of functions, variables or classes to the top of their scope, prior to execution of the code.

Hoisting allows functions to be safely used in code before they are declared.

Variable and class declarations are also hoisted, so they too can be referenced before they are declared. Note that doing so can lead to unexpected errors, and is not generally recommended.
```
Note: The term hoisting is not used in any normative specification prose prior to ECMAScript® 2015 Language Specification. Hoisting was thought up as a general way of thinking about how execution contexts (specifically the creation and execution phases) work in JavaScript.
```
## Functional Hoisting
One of the advantages of hoisting is that it lets you use a function before you declare it in your code.
```js
catName("Tiger");

function catName(name) {
  console.log(`My cat's name is ${name}`);
}
/*
The result of the code above is: "My cat's name is Tiger"
*/
```
Without hoisting you would have to write the same code like this:
```js
function catName(name) {
  console.log(`My cat's name is ${name}`);
}

catName("Tiger");
/*
The result of the code above is the same: "My cat's name is Tiger"
*/
```
## Variable hoisting
Hoisting works with variables too, so you can use a variable in code before it is declared and/or initialized.

However, JavaScript only hoists declarations, not initializations! This means that initialization doesn't happen until the associated line of code is executed, even if the variable was originally initialized then declared, or declared and initialized in the same line.

Until that point in the execution is reached the variable has its default initialization (`undefined` for a variable declared using `var`, otherwise uninitialized).
```
Note: Conceptually variable hoisting is often presented as the interpreter "splitting variable declaration and initialization, and moving (just) the declarations to the top of the code".
```
Below are some examples showing what can happen if you use a variable before it is declared.
## `var` hoisting
Here we declare and then initialize the value of a `var` after using it. The default initialization of the `var` is `undefined`.
```js
console.log(num); // Returns 'undefined' from hoisted var declaration (not 6)
var num; // Declaration
num = 6; // Initialization
console.log(num); // Returns 6 after the line with initialization is executed.

```
The same thing happens if we declare and initialize the variable in the same line.
```js
console.log(num); // Returns 'undefined' from hoisted var declaration (not 6)
var num = 6; // Initialization and declaration.
console.log(num); // Returns 6 after the line with initialization is executed.
```
If we forget the declaration altogether (and only initialize the value) the variable isn't hoisted. Trying to read the variable before it is initialized results in a ReferenceError exception.
```js
console.log(num); // Throws ReferenceError exception - the interpreter doesn't know about `num`.
num = 6; // Initialization
```
Note however that initialization also causes declaration (if not already declared). The code snippet below will work, because even though it isn't hoisted, the variable is initialized and effectively declared before it is used.
```js
a = "Cran"; // Initialize a
b = "berry"; // Initialize b

console.log(`${a}${b}`); // 'Cranberry'
```
## `let` and `const` hoisting
Variables declared with `let` and `const` are also hoisted but, unlike `var`, are not initialized with a default value. An exception will be thrown if a variable declared with `let` or `const` is read before it is initialized.
```js
console.log(num); // Throws ReferenceError exception as the variable value is uninitialized
let num = 6; // Initialization
```
Note that it is the order in which code is executed that matters, not the order in which it is written in the source file. The code will succeed provided the line that initializes the variable is executed before any line that reads it.
For information and examples see [`let` > temporal dead zone](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let#temporal_dead_zone_tdz).

## `Class` Hoisting
Classes defined using a [class declaration](/14_Classes/Classes.md#class-declaration) are hoisted, which means that JavaScript has a reference to the class. However the class is not initialized by default, so any code that uses it before the line in which it is initialized is executed will throw a `ReferenceError`.  
## Function and class expression hoisting
[Function expressions](/10_Functions/Functions.md#functional-declaration) and [class expressions](/14_Classes/Classes.md#class-expressions) are not hoisted.
The expressions evaluate to a function or class (respectively). They are typically then assigned to a variable or passed to other functions. In this case, the variable declaration is hoisted and the expression is its initialization. Therefore the expressions are not evaluated until the relevant line is executed.
# Variable Declaration
To use a variable, you've first got to create it — more accurately, we call this declaring the variable. To do this, we type the keyword `let` followed by the name you want to call your variable:
```js
let myName;
let myAge;
```
Here we're creating two variables called `myName` and `myAge`. Try typing these lines into your web browser's console. After that, try creating a variable (or two) with your own name choices.
```
Note: In JavaScript, all code instructions should end with a semicolon (;) — your code may work correctly for single lines, but probably won't when you are writing multiple lines of code together. Try to get into the habit of including it.
```
You can test whether these values now exist in the execution environment by typing just the variable's name, e.g.
```js
myName;
myAge;
```
They currently have no value; they are empty containers. When you enter the variable names, you should get a value of `undefined` returned. If they don't exist, you'll get an error message — try typing in
```js
scoobyDoo;
```
```
Note: Don't confuse a variable that exists but has no defined value with a variable that doesn't exist at all — they are very different things. In the box analogy you saw above, not existing would mean there's no box (variable) for a 
value to go in. No value defined would mean that there is a box, but it has no value inside it.
```
### Initializing a Variable
Once you've declared a variable, you can initialize it with a value. You do this by typing the variable name, followed by an equals sign `=`, followed by the value you want to give it. For example:
```js
myName = 'Chris';
myAge = 37;
```
Try going back to the console now and typing in these lines. You should see the value you've assigned to the variable returned in the console to confirm it, in each case. Again, you can return your variable values by typing their name into the console — try these again:
```js
myName;
myAge;
```
You can declare and initialize a variable at the same time, like this:
```js
let myDog = 'Rover';
```
This is probably what you'll do most of the time, as it is quicker than doing the two actions on two separate lines.

## var
The `var` statement declares a function-scoped or globally-scoped variable, optionally initializing it to a value.

### Syntax
```js
var varname1 [= value1] [, varname2 [= value2] ... [, varnameN [= valueN]]]
```
#### `varname`

Variable name. It can be any legal identifier.
#### `valueN`
Initial value of the variable. It can be any legal expression. Default value is `undefined`.
Alternatively, the [Destructuring Assignment](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment) syntax can also be used to declare variables.
```js
var { bar } = foo; // where foo = { bar:10, baz:12 };
/* This creates a variable with the name 'bar', which has a value of 10 */
```
#### Description
`var` declarations, wherever they occur, are processed before any code is executed. This is called [hoisting](#hoisting) and is discussed further below.

The scope of a variable declared with `var` is its current execution context and closures thereof, which is either the enclosing function and functions declared within it, or, for variables declared outside any function, global. Duplicate variable declarations using `var` will not trigger an error, even in strict mode, and the variable will not lose its value, unless another assignment is performed.
```js
'use strict';
function foo() {
  var x = 1;
  function bar() {
    var y = 2;
    console.log(x); // 1 (function `bar` closes over `x`)
    console.log(y); // 2 (`y` is in scope)
  }
  bar();
  console.log(x); // 1 (`x` is in scope)
  console.log(y); // ReferenceError in strict mode, `y` is scoped to `bar`
}

foo();
```
Variables declared using `var` are created before any code is executed in a process known as hoisting. Their initial value is `undefined`.
```js
'use strict';
console.log(x);                // undefined (note: not ReferenceError)
console.log('still going...'); // still going...
var x = 1;
console.log(x);                // 1
console.log('still going...'); // still going...
```
In the global context, a variable declared using var is added as a non-configurable property of the global object. This means its property descriptor cannot be changed and it cannot be deleted using [`delete`](/9_Expressions%20and%20Operators/Readme.md#delete-operator). The corresponding name is also added to a list on the internal `[[VarNames]]` slot on the [global environment record](https://tc39.es/ecma262/#sec-global-environment-records) (which forms part of the global lexical environment). The list of names in `[[VarNames]]` enables the runtime to distinguish between global variables and straightforward properties on the global object.

The property created on the global object for global variables, is set to be non-configurable because the identifier is to be treated as a variable, rather than a straightforward property of the global object. JavaScript has automatic memory management, and it would make no sense to be able to use the delete operator on a global variable.
```js
'use strict';
var x = 1;
Object.hasOwn(globalThis, 'x'); // true
delete globalThis.x; // TypeError in strict mode. Fails silently otherwise.
delete x;  // SyntaxError in strict mode. Fails silently otherwise.
```
Note that in both NodeJS [CommonJS](https://www.commonjs.org/) modules and native ECMAScript modules, top-level variable declarations are scoped to the module, and are not, therefore added as properties to the global object.
### Unqualified identifier assignments
The global object sits at the top of the scope chain. When attempting to resolve a name to a value, the scope chain is searched. This means that properties on the global object are conveniently visible from every scope, without having to qualify the names with `globalThis`. or `window`. or `global`..

Because the global object has a `String` property `(Object.hasOwn(globalThis, 'String'))`, you can use the following code:
```js
function foo() {
  String('s') // Note the function `String` is implicitly visible
}
```
o the global object will ultimately be searched for unqualified identifiers. You don't have to type `globalThis.String`, you can just type the unqualified `String`. The corollary, in non-strict mode, is that assignment to unqualified identifiers will, if there is no variable of the same name declared in the scope chain, assume you want to create a property with that name on the global object.
```js
foo = 'f' // In non-strict mode, assumes you want to create a property named `foo` on the global object
Object.hasOwn(globalThis, 'foo') // true
```
In [strict mode](/11_Strict%20Mode/Readme.md#strict-mode), assignment to an unqualified identifier in strict mode will result in a `ReferenceError`, to avoid the accidental creation of properties on the global object.

Note that the implication of the above, is that, contrary to popular misinformation, JavaScript does not have implicit or undeclared variables, it merely has a syntax that looks like it does.

### var Hoisting
Because `var`declarations are processed before any code is executed, declaring a variable anywhere in the code is equivalent to declaring it at the top. This also means that a variable can appear to be used before it's declared. This behavior is called "hoisting", as it appears that the variable declaration is moved to the top of the function or global code.
```js
bla = 2;
var bla;
```
This is implicitly understood as:

```js

var bla;
bla = 2;

```
For that reason, it is recommended to always declare variables at the top of their scope (the top of global code and the top of function code) so it's clear which variables are function scoped (local) and which are resolved on the scope chain.

It's important to point out that only a variable's declaration is hoisted, not its initialization. The initialization happens only when the assignment statement is reached. Until then the variable remains `undefined` (but declared):
```js
function do_something() {
  console.log(bar); // undefined
  var bar = 111;
  console.log(bar); // 111
}
```
This is implicitly understood as:
```js
function do_something() {
  var bar;
  console.log(bar); // undefined
  bar = 111;
  console.log(bar); // 111
}
```
### ***Examples***
1. Declaring and initializing two variables:
```js
var a = 0, b = 0;
```
2. Assigning two variables with single string value
```js
var a = 'A';
var b = a;
```
This is equivalent to:
```js
var a, b = a = 'A';
```
Be mindful of the order:
```js
var x = y, y = 'A';
console.log(x + y); // undefinedA
```
Here, `x` and `y` are declared before any code is executed, but the assignments occur later. At the time `x = y` is evaluated, `y` exists so no `ReferenceError` is thrown and its value is `undefined`. So, `x` is assigned the undefined value. Then, `y` is assigned the value `'A'`. Consequently, after the first line, `x === undefined && y === 'A'`, hence the result.
3. Initialization of several variables
```js
var x = 0;
function f() {
  var x = y = 1; // Declares x locally; declares y globally.
}
f();

console.log(x, y); // 0 1

// In non-strict mode:
// x is the global one as expected;
// y is leaked outside of the function, though!
```
The same example as above but with a strict mode:

```js
'use strict';

var x = 0;
function f() {
  var x = y = 1; // Throws a ReferenceError in strict mode.
}
f();

console.log(x, y);
```
4. Implicit globals and outer function scope
Variables that appear to be implicit globals may be references to variables in an outer function scope:
```js
var x = 0; // Declares x within file scope, then assigns it a value of 0.

console.log(typeof z); // "undefined", since z doesn't exist yet

function a() {
  var y = 2; // Declares y within scope of function a, then assigns it a value of 2.

  console.log(x, y); // 0 2

  function b() {
    x = 3; // Assigns 3 to existing file scoped x.
    y = 4; // Assigns 4 to existing outer y.
    z = 5; // Creates a new global variable z, and assigns it a value of 5.
           // (Throws a ReferenceError in strict mode.)
  }

  b(); // Creates z as a global variable.
  console.log(x, y, z); // 3 4 5
}

a(); // Also calls b.
console.log(x, z);     // 3 5
console.log(typeof y); // "undefined", as y is local to function a
```
## const
Constants are [block-scoped](#block-scope), much like variables declared using the [`let`](#let) keyword. The value of a constant can't be changed through reassignment (i.e. by using the [assignment operator](#the-assignment-operator)), and it can't be redeclared (i.e. through a [variable declaration](#variable-declaration)). However, if a constant is an [object](/3_Data%20Types/Data%20Types.md#object) or array its properties or items can be updated or removed.
### Syntax
```js
const name1 = value1 [, name2 = value2 [, ... [, nameN = valueN]]]
```
#### nameN
The constant's name, which can be any legal identifier.
The [destructuring assignment](/9_Expressions%20and%20Operators/Readme.md#destructuring-assignment) syntax can also be used to declare variables.
```js
const { bar } = foo; // where foo = { bar:10, baz:12 };
/* This creates a constant with the name 'bar', which has a value of 10 */
```
### Description
This declaration creates a constant whose scope can be either global or local to the block in which it is declared. Global constants do not become properties of the [`window`](https://developer.mozilla.org/en-US/docs/Web/API/Window) object, unlike [`var`](#var) variables.

An initializer for a constant is required. You must specify its value in the same declaration. (This makes sense, given that it can't be changed later.)

The `const` declaration creates a read-only reference to a value. It does not mean the value it holds is immutable—just that the variable identifier cannot be reassigned. For instance, in the case where the content is an object, this means the object's contents (e.g., its properties) can be altered.

All the considerations about the [temporal dead zone](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let#temporal_dead_zone_tdz) apply to both `let` and `const`.

A constant cannot share its name with a function or a variable in the same scope.

Unlike `var`, `const` begins [declarations, not statements](/10_Functions/Functions.md#diffrence-betweem-declarations-and-statements). That means you cannot use a lone `const` declaration as the body of a block (which makes sense, since there's no way to access the variable).
```js
if (true) const a = 1; // SyntaxError: Unexpected token 'const'
```
### ***Examples***
1. Basic const usage
Constants can be declared with uppercase or lowercase, but a common convention is to use all-uppercase letters.
```js
// define MY_FAV as a constant and give it the value 7
const MY_FAV = 7;

// this will throw an error - Uncaught TypeError: Assignment to constant variable.
MY_FAV = 20;

// MY_FAV is 7
console.log('my favorite number is: ' + MY_FAV);

// trying to redeclare a constant throws an error
// Uncaught SyntaxError: Identifier 'MY_FAV' has already been declared
const MY_FAV = 20;

// the name MY_FAV is reserved for constant above, so this will fail too
var MY_FAV = 20;

// this throws an error too
let MY_FAV = 20;
```
2. Block scoping
It's important to note the nature of block scoping.
```js
if (MY_FAV === 7) {
  // this is fine and creates a block scoped MY_FAV variable
  // (works equally well with let to declare a block scoped non const variable)
  let MY_FAV = 20;

  // MY_FAV is now 20
  console.log('my favorite number is ' + MY_FAV);

  // this gets hoisted into the global context and throws an error
  var MY_FAV = 20;
}

// MY_FAV is still 7
console.log('my favorite number is ' + MY_FAV);
```
3. const needs to be initialized
```js
// throws an error
// Uncaught SyntaxError: Missing initializer in const declaration

const FOO;
```
4. const in objects and arrays
`const` also works on objects and arrays. Attempting to overwrite the object throws an error "Assignment to constant variable".
```js
const MY_OBJECT = { key: 'value' };
MY_OBJECT = { OTHER_KEY: 'value' };
```
However, object keys are not protected, so the following statement is executed without problem.
```js
MY_OBJECT.key = 'otherValue';
```
You would need to use [Object.freeze()](/3_Data%20Types/Data%20Types.md#object.freeze()) to make an object immutable.

The same applies to arrays. Assigning a new array to the variable throws an error "Assignment to constant variable".
```js
const MY_ARRAY = [];
MY_ARRAY = ['B'];
```
Still, it's possible to push items into the array and thus mutate it.
```js
MY_ARRAY.push('A'); // ["A"]
```
## let
# Variables Scopes
Before ES6 (2015), JavaScript had only Global Scope and Function Scope. ES6 introduced two important new JavaScript keywords: `let` and `const`. These two keywords provide Block Scope in JavaScript.


## Block Scope
This scope restricts the variable that is declared inside a specific block, from access by the outside of the block. The let & const keyword facilitates the variables to be block scoped. In order to access the variables of that specific block, we need to create an object for it. Variables declared with the var keyword, do not have block scope.
In this article, we will see what is Block scoping in Javascript, access to the block-scoped variables, how it is distinct from other kinds of variable’s scope, through the examples. Prior to [ES2015](/1_Introduction/Introduction.md#release-of-es6--ecmascript-2015), JavaScript supported only function-level scoping unlike other languages like C++/Java which has block-level scoping. With [ES2015](/1_Introduction/Introduction.md#release-of-es6--ecmascript-2015), in addition to function-level scoping, JavaScript also supports block-level scoping with the help of the [let keyword](#let) & [const keyword](#const).

But before we get into details of [ES2015](/1_Introduction/Introduction.md#release-of-es6--ecmascript-2015) stuff, let’s discuss what we exactly mean by phrases “function-level scope” and “block-level scope”.

Block Level Scope: This scope restricts the variable that is declared inside a specific block, from access by the outside of the block. The let & const keyword facilitates the variables to be block scoped. In order to access the variables of that specific block, we need to create an object for it. Variables declared with the var keyword, do not have block scope.

For instance, consider the below example:
```js
{
   let p = 110;
   const q = 111;
}
console.log(p); // Uncaught ReferenceError: p is not defined
console.log(q); // Uncaught ReferenceError: q is not defined
```
Here, we have used the let & const keyword to illustrate the block-level scope, in order to access the variable from outside of the block.

***Function level Scope:*** The variables in this scope level are restricted to access only the inside the function where it is declared ie., it can be accessed anywhere inside of that function, not accessible outside functions. Every time a new scope will be generated while creating a function & in that scope, any variable can be accessed by any function within that scope. The function or variables defined as global scope will be accessible by all the other variables or functions. Now, let’s look at the function scope in JavaScript.
```js
function printIfGFG( text){
   if(text=="GeeksforGeeks"|| text=="GFG") {
   var message = "Verified Geek";
   console.log(message); // Output: Verified Geek
}
console.log(message); // Output: Verified Geek
}
printIfGFG("GFG");
```
In the code snippet above, we have declared and defined a variable message inside the [if-condition](/8_Control%20Flow/Readme.md#if). Then, displayed the output the value using [`console.log()`](/10_Functions/Functions.md#consolelog-function) function.

The tricky part is the fact that we can also able to print the value of variable ‘message’ outside the if-condition. This is because in JavaScript functions declared using the keyword ‘var’ have to function scope, by default. JavaScript runtime looks for the closest enclosing function relative to the variable declaration and sets it as the scope for that variable.

But, how JavaScript runtime does this? Well, it is worth mentioning here that JavaScript runtime internally changes our code and moves all [variable declarations](#variable-hoisting) to the starting of the function. This is known as variable hoisting. So, our code in the current example is effectively changed to the below code snippet.
## Local Scope
Variables declared within a JavaScript function, become LOCAL to the function.
```js
// code here can NOT use carName

function myFunction() {
  let carName = "Volvo";
  // code here CAN use carName
}

// code here can NOT use carName
```
```
NOTE: Local variables have Function Scope:

They can only be accessed from within the function.
```


## Functional Scope
JavaScript has function scope: Each function creates a new scope.
Variables defined inside a function are not accessible (visible) from outside the function.
Variables declared with `var`, `let` and `const` are quite similar when declared inside a function.
They all have **Function Scope**:
```js
function myFunction() {
  var carName = "Volvo";   // Function Scope
}
```
```js
function myFunction() {
  let carName = "Volvo";   // Function Scope
}
```
```js
function myFunction() {
  const carName = "Volvo";   // Function Scope
}
```
In this article, we will cover all the basic concepts of JS functions, callbacks, scopes, closures in-depth which would help you to –
- understand different types of functions declaration.
- make better use of functions.
- understand how different scopes and scope chain works in JS.
- learn about closures and how to use them.
We will understand all these concepts through the examples & also understand their implementations. Let’s begin the discussion with Javascript Function.

Functions: [Function](/10_Functions/Functions.md#functions) allows us to declare & pack a bunch of code in a block so that we can use (and reuse) a block of code in our programs. Sometimes, they take some values as `parameters` to do the operation and return some value as a result of the operation.

Example:
```js
function add(a, b) {

	// a and b are the parameters of this
	// function code to do the operation
	return a + b; // return statement
}

// Invoking the function and 2, 3
// are arguments here
add(2, 3);
```
Output:
```
5
```
First-Class Citizen: If any programming language has the ability to treat functions as values, to pass them as arguments and to return a function from another function then it is said that programming language has First Class Functions and the functions are called [First-Class Citizens](https://www.geeksforgeeks.org/what-is-first-class-citizen-in-javascript/) in that programming language. Functions will be considered as First-Class Citizen in JavaScript if the functions:

- store functions in a variable.
- pass a function as an argument to another function.
- return a function from another function.
Function Expressions: When a function is stored inside a variable, it is called a function expression. This can be named or anonymous. If a function doesn’t have any name and is stored in a variable, then it would be known as an anonymous function expression. Otherwise, it would be known as a named [function expression](/10_Functions/Functions.md#functional-expresions). Please refer to the JavaScript Function expression article for more details
Example:
```js
// Anonymous function expression
const add = function (a, b){
	return a + b;
}

// Named function expression
const subtractResult = function subtract(a, b){
	return a - b;
}

console.log(add(3, 2)); // 5
console.log(subtractResult(3, 2)); // 1
```
The output will be 5 & 1 respectively.

**Callbacks:** Storing a function in a variable makes it really easy to pass a function to another function as an argument. A function that takes other functions as arguments or returns a function is known as a **higher-order function**. A function that is passed as an argument into another function is known as a [callback function](/13_Asynchronous%20JavaScript/Readme.md#callback). In simple words, If we want to execute a function right after the return of some other function, then callbacks can be used. Please refer to the JavaScript | Callbacks article for more details.

Example:
```js
function showLength(name, callback) {
callback(name);
}

// function expression `nameLength`
const nameLength = function (name) {
console.log(`Given Name ${name} which
is ${name.length} chars long`);
};

// Passing `nameLength` as a callback function
showLength("GeeksforGeek", nameLength);
```
Output:
```
Given Name GeeksforGeek which is 12 characters long
```
## Global Scope
