
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
***The Assignment Operator***

In JavaScript, the equal sign (=) is an "assignment" operator, not an "equal to" operator.

This is different from algebra. The following does not make sense in algebra:
```js
x = x + 5
```
In JavaScript, however, it makes perfect sense: it assigns the value of x + 5 to x.

(It calculates the value of x + 5 and puts the result into x. The value of x is incremented by 5.)


**Note**

The "equal to" operator is written like == in JavaScript.




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
## let
# Variables Scopes
## Block Scope
## Local Scope
## Functional Scope
## Global Scope