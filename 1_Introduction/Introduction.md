# Introduction to Javascript

## Overview.

- [Introduction to Javascript](#introduction-to-javascript)
  - [what is Javascript?](#what-is-javascript)
  - [History of Javascript.](#history-of-javascript)
  - [Javascript Versions.](#javascript-versions)
  - [How to run Javascript?](#how-to-run-javascript)

For more Free Content on Variables Visit


# What is Javascript?
JavaScript (JS) is a lightweight, interpreted, or just-in-time compiled programming language with first-class functions. While it is most well-known as the scripting language for Web pages, many non-browser environments also use it, such as Node.js, Apache CouchDB and Adobe Acrobat. JavaScript is a prototype-based, multi-paradigm, single-threaded, dynamic language, supporting object-oriented, imperative, and declarative (e.g. functional programming) styles. Read more about JavaScript.

This section is dedicated to the JavaScript language itself, and not the parts that are specific to Web pages or other host environments. For information about APIs that are specific to Web pages, please see [Web APIs](https://developer.mozilla.org/en-US/docs/Web/API) and [DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model).

The standards for JavaScript are the ECMAScript Language Specification (ECMA-262) and the ECMAScript Internationalization API specification (ECMA-402). As soon as one browser implements a feature, we try to document it. This means that cases where some proposals for new ECMAScript features have already been implemented in browsers, documentation and examples in MDN articles may use some of those new features. Most of the time, this happens between the stages 3 and 4, and is usually before the spec is officially published.

Do not confuse JavaScript with the Java programming language. Both "Java" and "JavaScript" are trademarks or registered trademarks of Oracle in the U.S. and other countries. However, the two programming languages have very different syntax, semantics, and use.


# History of Javascript.
Around 10 years ago, Jeff Atwood (the founder of stackoverflow) made a case that JavaScript is going to be the future and he coined the “Atwood Law” which states that Any application that can be written in JavaScript will eventually be written in JavaScript. Fast-forward to today, 10 years later, if you look at it it rings truer than ever. JavaScript is continuing to gain more and more adoption.


## JavaScript is announced
JavaScript was initially created by [Brendan Eich](https://twitter.com/BrendanEich) of NetScape and was first announced in a press release by Netscape in 1995. It has a bizarre history of naming; initally it was named `Mocha` by the creator, which was later renamed to `LiveScript`. In 1996, about a year later after the release, NetScape decided to rename it to be `JavaScript` with hopes of capitalizing on the Java community (although JavaScript did not have any relationship with Java) and released Netscape 2.0 with the official support of JavaScript.


## ES1, ES2 and ES3
In 1996, Netscape decided to submit it to [ECMA International](https://en.wikipedia.org/wiki/Ecma_International) with the hopes of getting it standardized. First edition of the standard specification was released in 1997 and the language was standardized. After the initial release, `ECMAScript` was continued to be worked upon and in no-time two more versions were released ECMAScript 2 in 1998 and ECMAScript 3 in 1999.


## Decade of Silence and ES4
After the release of ES3 in 1999, there was a complete silence for a decade and no changes were made to the official standard. There was some work on the fourth edition in the initial days; some of the features that were being discussed included classes, modules, static typings, destructuring etc. It was being targeted to be released by 2008 but was abandoned due to political differences concerning language complexity. However, the vendors kept introducing the extensions to the language and the developers were left scratching their heads — adding polyfills to battle compatibility issues between different browsers.

## From silence to ES5
Google, Microsoft, Yahoo and other disputers of ES4 came together and decided to work on a less ambitious update to ES3 tentatively named ES3.1. But the teams were still fighting about what to include from ES4 and what not. Finally, in 2009 ES5 was released mainly focusing on fixing the compatibility and security issues etc. But there wasn’t much of a splash in the water — it took ages for the vendors to incorporate the standards and many developers were still using ES3 without being aware of the “modern” standards.

## Release of ES6 — ECMAScript 2015
After a few years of the release of ES5, things started to change, TC39 (the committee under ECMA international responsible for ECMAScript standardization) kept working on the next version of ECMAScript (ES6) which was originally named ES Harmony, before being eventually released with the name ES2015. ES2015 adds significant features and syntactic sugar to allow writing complex applications. Some of the features that ES6 has to offer, include Classes, Modules, Arrows, Enhanced object literals, Template strings, Destructuring, Default param values + rest + spread, Let and Const, Iterators + for..of, Generators, Maps + Sets, Proxies, Symbols, Promises, math + number + string + array + object APIs [etc](http://es6-features.org/#Constants)

Browser support for ES6 is still scarce but everything that ES6 has to offer is still available to developers by transpiling the ES6 code to ES5. With the release of 6th version of ECMAScript, TC39 decided to move to yearly model of releasing updates to ECMAScript so to make sure that the new features are added as soon as they are approved and we don’t have to wait for the full specification to be drafted and approved — thus 6th version of ECMAScript was renamed as ECMAScript 2015 or ES2015 before the release in June 2015. And the next versions of ECMAScript were decided to published in June of every year.


## Release of ES7 — ECMAScript 2016
In June 2016, seventh version of ECMAScript was released. As ECMAScript has been moved to an yearly release model, ECMAScript 2016 (ES2016) comparatively did not have much to offer. ES2016 includes just two new features

- Exponentiation operator `**`
- `Array.prototype.includes`

## What is ESNext then?
ESNext is a dynamic name that refers to whatever the current version of ECMAScript is at the given time. For example, at the time of this writing `ES2017` or `ES8` is `ESNext`.

## What does the future hold?
Since the release of ES6, [TC39](https://github.com/tc39) has quite streamlined their process. TC39 operates through a Github organization now and there are [several proposals](https://github.com/tc39/proposals) for new features or syntax to be added to the next versions of ECMAScript. Any one can go ahead and [submit a proposal](https://github.com/tc39/proposals) thus resulting in increasing the participation from the community. Every proposal goes through [four stages of maturity](https://tc39.es/process-document/) before it makes it into the specification.
h
Here are the links to original language specifications [ES6](https://262.ecma-international.org/6.0/), [ES7](https://262.ecma-international.org/7.0/) and [ES8](https://262.ecma-international.org/8.0/).


**For more Free History Javascipt follow the Links**

- [History of JS](https://dev.to/iarchitsharma/the-history-of-javascript-5e98)

# Javascript Versions.
JavaScript was invented by Brendan Eich, and in 1997 and became an ECMA standard. ECMAScript is the official language name. ECMAScript versions include ES1, ES2, ES3, ES5, and ES6

| Version | Official Name       | Description                                                                                   |
|---------|---------------------|-----------------------------------------------------------------------------------------------|
| ES1     | ECMAScript 1 (1997) | First edition                                                                                 |
| ES2     | ECMAScript 2 (1998) | Editorial changes                                                                             |
| ES3     | ECMAScript 3 (1999) | Added regular expressions & try/catch                                                         |
| ES4     | ECMAScript 4        | Not released                                                                                  |
| ES5     | ECMAScript 5 (2009) | Added “strict mode”, JSON support, String.trim(), Array.isArray(), & Array iteration methods. |
| ES6     | ECMAScript 2015     | Added let and const, default parameter values, Array.find(), & Array.findIndex()              |
| ES6     | ECMAScript 2016     | Added exponential operator & Array.prototype.includes                                         |
| ES6     | ECMAScript 2017     | Added string padding, Object.entries, Object.values, async functions, & shared memory         |
| ES6     | ECMAScript 2018     | Added rest / spread properties, asynchronous iteration, Promise.finally(), & RegExp           |


## ECMAScript 1-4
ECMAScript 1 (ES1) was released in 1997 with ES2 following the following year. Not much changed between the two versions.
## ES3
ES3 was released in 1999 and added support for many new things that have become a standard part of the language today:

- **Strict Equality:** Beginning with ES3, the strict equality operator ( === ) became an option to use in addition to the equality operator ( == ). The difference between the two is a matter of comparing the type and number. Strict equality considers values that are the same but a different type to be unequal.
```js
const compareTypeAndValue = (num, str) => {
 return num === str;
}
 
console.log(compareTypeAndValue(8, '8')); //false
console.log(compareTypeAndValue(8, 8)); //true
```
- **Regular Expressions:** Two types of regular expressions became available in ES3: literal and constructor.
- **Literal Expressions:** Literal regular expressions are expressed in between two backslashes. The actual expression is in between the slashes and the global, ignore case, and multi-line flags can be turned on or off after the last backslash.
```js
/[^abc]/gim
```
- **Constructor Expressions:** Constructor regular expressions are those expressions that are created as an instance of the RegExp object. The actual regular expression is the first argument that is passed into the RegExp constructor. The second, if needed, are the flags you would like to use.
```js
const regex = new RegExp(‘[^abc]’, ‘gim’);
``` 
- **Switch Statement:** The switch statement is a control flow statement that basically chains together many if conditions without having to use else if statements. The switch statement uses a parameter and compares that parameter to each of the case statements. If that parameter matches a case, it performs the logic in that block.

```js
const fizzBuzz = (num) => {
 
    switch(num) {
     case 1:
       console.log(num);
       break;
     case 2:
       console.log(num);
       break;
     case 3:
       console.log("fizz");
       break;
     case 4:
       console.log(num);
       break;
     case 5:
       console.log("buzz");
       break;
     case 6:
       console.log("fizz");
       break;
     case 7:
       console.log(num);
       break;
     case 8:
       console.log(num);
       break;
     case 9:
       console.log("fizz");
       break;
     case 10:
       console.log(num);
       break;
   }
}
 
console.log(fizzBuzz(3))
```
- **Try/Catch Handling:** A try/catch handler will throw an error if the try block for whatever reason fails. Below, the try fails because obj was never defined. The catch block is executed and a new Error object exception is thrown.
```js
const isValidKey = (val1) => {
try {
  let obj;
 
  return obj.hasOwnProperty(val1);
 
} catch (err) {
    throw new Error("not valid key");
}
}
console.log(isValidKey(""))
```
```
ES3 was the last major update to the ECMAScript specification for almost a decade, until 2009 with ES5.
```
## ES4
TC39 is a Royalty-Free Task Group at ECMA International whose main job is to standardize ECMAScript. When it came time to update and release a standard for ES4, the task group really couldn’t agree on a specification. As a result, ES4 was dog-eared as a version, but never fully released as an actual standard.
## ECMAScript 5 updates in detail
ES5 and ES6 are the latest specifications released that have had the greatest number of changes.

Ten years after the release of ES3, in 2009, a new version of ECMAScript was released. This standard was the biggest change to JavaScript since its founding. Some of the new features include:

### “use strict”
Prior to ES5, undeclared variables (those variables that don’t use the var keyword when initially introduced), were allowed to be used. When the “use strict” feature is turned on, a reference error is thrown.
```js
"use strict"
 
x = 5; // ReferenceError: x is not defined
```
### New Array Methods
There are several new array methods that were introduced in ES5 that made life much easier when working with arrays. The new array methods are shown here in alphabetical order:

#### `every()`
The `every()` array method checks to see if every single element in the array satisfies the condition you have passed it.
```js
var arr = [6, 4, 5, 6, 7, 7];
 
arr.every(function(element) {
 return element % 2 === 0; //checks to see if even
}); // false
```
#### `filter()`
Think of the filter method as a for loop that has an if statement. If the element passes the test, you push that element to a new array. This is how `filter()` works under the hood.

Like `map()`, another array method mentioned in this section, `filter()` returns a new array with the values that pass the test.
```js
var arr = [6, 4, 5, 6, 7, 7];
 
arr.filter(function(element) {
 return element/2 > 3;
})
```
#### `forEach()`
A method that is very similar to a for loop. For every element found in the array, the `forEach()` method executes a callback function on it.
```js
var arr = [6, 4, 5, 6, 7, 7];
 
arr.forEach(function(element) {
 console.log(element * 2);
})

```
#### `indexOf()` and `lastIndexOf()`
If you need to search for a particular element in an array, you can do that with `indexOf()` and `lastIndexOf()`. `indexOf()` returns the first index of the search parameter if it’s found, otherwise it returns a -1.

In `lastIndexOf()`, it gives us the last index of the search element in the array. Again, if not found, it’ll return `-1`.
```js
var arr = [6, 4, 5, 6, 7, 7];
 
console.log(arr.indexOf(4)); // 1
console.log(arr.indexOf(2)); // -1
console.log(arr.indexOf(7)); // 4
 
console.log(arr.lastIndexOf(7)); // 5
```
#### `isArray()`
This method checks to see if the object passed to it is an array or not. Returns a boolean.
```js
var arr = [6, 4, 5, 6, 7, 7];
 
var str = "Hello Educative.io";
 
console.log(Array.isArray(arr));
console.log(Array.isArray(str));
```
#### `map()`
The `map()` method is very similar to the `forEach()` method with the exception that it returns a brand new array. This allows for manipulation of data without compromising the original array.

The callback function must have a return statement. This is the new value that will be going into that particular index of the new array.
```js
var arr = [6, 4, 5, 6, 7, 7];
 
arr.map(function(element) {
 return element * 2;
})
```
#### `reduce()` and `reduceRight()`
Each of these reduce methods applies a callback function to each element in the array. What is special about the `reduce()` and `reduceRight()` methods is that it reduces the array to a single element.

The `reduceRight()` method is just like `reduce()` except that it iterates from right to left instead of left to right.
```js
var arr = [6, 4, 5, 6, 7, 7];
 
var reduced = arr.reduce(function(curr, next) {
 return curr + next;
}, 0);
 
var reducedRight = arr.reduceRight(function(curr, next) {
 return curr + next;
}, 0)
 
console.log(reduced);
 
console.log(reducedRight);
```
#### `some()`
The `some()` method is almost exactly like the `every()` method, with the exception that it checks to see if at least one element satisfies the condition you have set for it.
```js
var arr = [6, 4, 5, 6, 7, 7];
 
arr.some(function(element) {
 return element % 2 === 0; //checks to see if even
}); //true
```
### JSON
The ability to parse and stringify JavaScript Object Notation (JSON) became a possibility in the ES5 standard. The JSON format is used to basically transmit some sort of structured data over a network connection, usually a web application and an API.

When we transmit the data from one application, it has to be in the form of a string. We use `JSON.stringify()` to transform JavaScript objects into strings.

We then use `JSON.parse()` on the other side, to transform the data after transmission back to a JavaScript object so we can use it.
```js
var arr = [6, 4, 5, 6, 7, 7];
var obj = {
 author: "Christina Kopecky",
 title: "How to parse JSON objects",
 published: false
}
console.log("======== ARR EXAMPLE ==========");
console.log("orig arr=====>", arr);
console.log("stringified arr=====>", JSON.stringify(arr));
console.log("proof of type=====>", typeof JSON.stringify(arr));
console.log("parsed string=====>", JSON.parse(JSON.stringify(arr)));
console.log("proof of type=====>", typeof JSON.parse(JSON.stringify(arr)), "\n\n");
 
console.log("======== OBJ EXAMPLE ==========");
console.log("orig obj=====>", obj);
console.log("stringified obj=====>", JSON.stringify(obj));
console.log("proof of type=====>", typeof JSON.stringify(obj));
console.log("parsed string=====>", JSON.parse(JSON.stringify(obj)));
console.log("proof of type=====>", typeof JSON.parse(JSON.stringify(obj)), "\n\n");
```
### New Date Methods
There were two new Date object methods that were introduced in ES5 that are functionally equivalent. They both return the current time in milliseconds since January 1, 1970. They are Date.now() and new Date().valueOf().

```js
console.log(Date.now());
 
console.log(new Date().valueOf());
```
The biggest difference between the two methods is that `valueOf()` is a method on an instance of the Date object and `Date.now()` is a static function of the Date object.
```
Note: Internet Explorer may not support `Date.now()`, so if that is a concern for you, you may need to deal with that in your code.
```
### getters and setters
In ES5, we are introduced to the idea of accessor properties. These are functions whose sole purpose is to get or set a value. They look like standard properties when you call them:
```js
let character = {
 first_name: "Darth",
 last_name: "Vader",
 
 get fullName() {
   return `${this.first_name} ${this.last_name}`;
 },
 set fullName(str) {
   [this.first_name, this.last_name] = str.split(" ");
 }
 
};
 
console.log(character.fullName); // Darth Vader
 
character.fullName = "Luke Skywalker"
 
console.log(character.first_name);
console.log(character.last_name);
```
The ES5 standard really started to pave the way for making JavaScript code more readable. With the introduction of new array methods, the ability to parse and stringify JSON, and making code creation more strict, it really helped make JavaScript easier to understand.
### ES6 updates in detail
Seven years passed between the finished version of ES5 to the release of ES6. It became a standard in June of 2015. 
#### Babel
One of the biggest changes from ES5 is that ES6 JavaScript is not able to be compiled directly in browsers. We need to use a transpiler called `Babel.js` to produce compatible JavaScript that the older browsers can read.
```
Babel allows you to use ES6 features and syntax in your project and then translates it to ES5 so that you can use it in production.
```
To use Babel when your project is built, you’ll need to add a package.json to your project. This is where all of your dependencies for your project will be held.

Be sure that you have Node and npm installed (or Node and Yarn installed if you prefer to use Yarn) and then type in the `npm init` or the `yarn init` command in your terminal. Answer the questions that come up and the `package.json` will be pre-filled with those values.

Use npm/yarn to add babel to your dependencies with the command:
```npm install --save-dev babel-cli
// or
yarn add babel-cli --dev
```
You’ll use the scripts field in your `package.json` to set your build command with Babel. The actual command will differ based upon the folder you are building from and where you want to build to.

Finally, in the root folder of your project (where the `package.json` resides), create a `.babelrc` file. This is a Babel configuration file that will tell Babel to transform your code to ES5. Install the preset with:
```
npm install --save-dev babel-preset-env
// or
yarn add babel-preset-env --dev
```
And then define it in your `.babelrc file`:
```
{
    “presets”: [“env”]
}
```
Now you can run Babel by running your build command. Your destination folder should now look exactly like your origin folder, except that the contents of the destination folder is ES5 code instead of ES6.

If you happen to use a JavaScript library or framework like create-react-app, more than likely the Babel is already configured for you and you won’t need to worry about it. This is for projects that are created from scratch.

#### Big Arrow (Fat Arrow) Functions
Before this new standard, JavaScript used the function keyword to create functions. Now, we can use the big arrow, `=>`, to write functions. It can make code look a little more elegant as we can create one-liner fat arrow functions.
```js
//pre ES-6
 
function add(num1, num2) {
 return num1 + num2;
}
 
//ES6 (implicit return)
const addImplicit = (num1, num2) => num1 + num2;
 
console.log(add(3, 4));
console.log(addImplicit(3, 4));
```
The ES6 one-liner has an implicit return. We don’t need the return keyword if the function is only one line. This also means there is no need for curly braces. If the function is more than one line, we would need curly braces and a return statement:

```js
//ES6 (explicit return)
 
const addExplicitReturn = (num1, num2) => {
 let sum = num1 + num2;
 return sum;
};
 
 
console.log(addExplicitReturn(3, 4));
```
It’s also important to note that when you are using classes, the arrow function is bound to the “this” keyword so there is no need to actually use the `bind()` method to bind the function to the class.
```
If using the function keyword, the method needs to be bound to the class with the `bind()` method.
```
#### Classes
Classes act as syntactic sugar on top of JavaScript’s Prototypes. Instead of [Prototypal Inheritance](https://www.educative.io/blog/understanding-and-using-prototypal-inheritance-in-javascript), they use Classical Inheritance with the `extends` keyword. Overall, it just cuts down on the amount of code, and spruces it up a bit.
```js
class StarWarsCharacter{
 constructor(attributes) {
   this.name = attributes.name;
   this.age = attributes.age;
   this.homePlanet = attributes.homePlanet;
 }
 
 getCharacter = () => `${this.name} is ${this.age} years old and is from ${this.homePlanet}.`;
}
 
const luke = new StarWarsCharacter({ name: "Luke Skywalker", age: 23, homePlanet: "Tatooine"});
 
luke.getCharacter();
 
class Heroes extends StarWarsCharacter {
 constructor(attributes) {
   super(attributes);
   this.favoriteVehicle = attributes.favoriteVehicle;
 }
  getFavoriteVehicle = () => `${this.name} is ${this.age} and their favorite vehicle is the ${this.favoriteVehicle}`;  
}
 
const hans = new Heroes({ name: "Hans Solo", age: 35, favoriteVehicle: "Millennium Falcon"});
 
console.log(hans.getFavoriteVehicle());
```
#### Destructuring
Object destructuring is a great way to reduce code clutter to make it more palatable. It allows us to “unpack” an object and use that unpacked value as the variable we refer to later in the code.
```js
const state = {
 name: "Luke Skywalker",
 age: 22,
 dark_side: false
}
 
console.log("before destructuring");
 
console.log(state.name); // notice the prefixed object name prior to each property
console.log(state.age);  // destructuring gets rid of this
console.log(state.dark_side);
 
 
const { name, age, dark_side } = state;
 
console.log("after destructuring");
console.log(name); // we can access using just the property name now!
console.log(age); 
console.log(dark_side);
```
In the “before destructuring” section, we have to use the object name in addition to the property we want to access that property. We can destructure it by pulling out the properties, put it in a set of curly braces and set it to the object name.

Be sure to use the const keyword in front of the curly braces. It allows for us to access these properties as variables instead of using dot notation on the actual object itself.
```
Array destructuring is done in a very similar fashion, but with square brackets instead of curly braces.
```
```js
const arr_state = [ "Luke Skywalker", 22, false];
 
console.log("before destructuring");
 
console.log(arr_state[0]); // notice the index number in bracket notation
console.log(arr_state[1]);  // destructuring gets rid of this
console.log(arr_state[2]);
 
console.log("\n\n\n")
const [ name, age, dark_side ] = arr_state; // assign a variable to each of the indexes in the array
 
console.log("after destructuring");
console.log(name); // we can access using just the variable name we created now!
console.log(age); 
console.log(dark_side);
```
##### `let` and `const`
In ES6, we have some new variable keywords that have essentially replaced the var keyword. Prior to ES6, JavaScript only had functional and global scope. With the addition of `let` and `const`, we now have block scope.
```js
let x = 5;
 
function blockExample() {
 let x = 2 //this is function scope;
 if(x >= 3) {
   let x = 10; // this is block scope
   console.log(x, "inside if block");''
 } else {
   let x = 1;
   console.log(x, "inside else block")
 }
 console.log(x, "inside function");
}
 
blockExample();
console.log(x, "global example");
```
The `let`keyword can be reassigned as needed. When used in the same scope, a redeclaration of the same variable will throw a syntax error.

This is an improvement upon the `var` keyword where you could redeclare variables with another value. This proved problematic when we had the same variable name with different values that produced unintended bugs.
```js
// pre-ES6: 
var x = 5;
var x = 120; //produces no errors


// ES6: 
let x = 5;
let x = 120; // produces a syntax error
```
The const keyword is useful when you have a variable that you have no intention of reassigning. It will throw an error if you try to reassign your const variable to another value.
#### Promises
Promises are a way to handle Asynchronous JavaScript programming in a better way. Before, asynchronous calls were made by using callback functions, which could make code convoluted and confusing really quickly.
```
Note: Promises wrap asynchronous logic in a net package to make code more readable.
```
```js
console.log("before promise")
let promise = new Promise((resolve, reject) => {
  let resolvedFlag = false;
//this is just a flag so we can intentionally throw the response to test logic
  console.log("this is eventually going to be an API call");
  resolvedFlag = true; //flip resolved to true once all console logs are done
 
  if(resolvedFlag) { //if resolved is true invoke the resolve function   
      
resolve("Promise resolved THIS IS THE RESPONSE");
 
  } else { // else invoke the reject function with a new Error object with message
    reject(new Error("Promise failed"));
    console.log("after promise");
  }
});
 
promise.then(resp => {
  console.log(resp); //promise response
})
```
#### rest and spread operators
The rest and spread operators are essentially the same syntax, but serve a different purpose. The rest operator is used before a function parameter to indicate multiple arguments should be assigned to that parameter.

```js
function restExample(a, ...b) {
 console.log(a); // 1
 console.log(b); // [2, 3, 4, 5, 6]
}
 
restExample(1, 2, 3, 4, 5, 6);
```
The spread operator uses the same syntax, but is instead used by arrays. It essentially takes the contents of the array, copies it so that it can be spread into the new structure. We can use the spread operator as a way to add something to an array without having to use `push()` or `unshift()`.
```js
function spreadExample(arr) {
 let newArr = [2, 4, 6, 8];
 console.log("arr", arr);
 let combinedArr = [...newArr, ...arr]; //this pushes the contents of newArr and the contens of arr into a one-dimensional combined array.
 let arrWithOtherContents = ["a", ...newArr, {b: "c", d: "e"}, true, ...arr];
 console.log(arrWithOtherContents);
 console.log("combined", combinedArr);
}
 
console.log(spreadExample([1, 3, 5, 7, 9]))
```
The spread operator works great when you need to work with an array but don’t want to manipulate the actual contents of the array. You can use the spread operator to create essentially a copy to work with.

#### Template Literals
In ES6, we no longer need to concatenate strings, spaces, and variables together to form a larger string. We use template literals to create expressions that allow us to have variables embedded in our strings.
```js
let name = "Jane";
let holiday = "Christmas";
 
//pre-ES6:
 
console.log(name + "'s favorite holiday is " + holiday);
 
//ES6+:
 
console.log(`${name}'s favorite holiday is ${holiday}`);
```


<d/>

# How to run Javascript?
## Requirements

No prior knowledge of programming is required to follow this challenge. You need only:

1. Motivation
2. A computer
3. Internet
4. A browser
5. A code editor

## Setup

I believe you have the motivation and a strong desire to be a developer, a computer and Internet. If you have those, then you have everything to get started.

### Install Node.js

You may not need Node.js right now but you may need it for later. Install [node.js](https://nodejs.org/en/).

![Node download](/images/download_node.png)

After downloading double click and install

![Install node](/images/install_node.png)

We can check if node is installed on our local machine by opening our device terminal or command prompt.

```sh
asabeneh $ node -v
v12.14.0
```

When making this tutorial I was using Node version 12.14.0, but now the recommended version of Node.js for download is v14.17.6, by the time you use this material you may have a higher Node.js version.

### Browser

There are many browsers out there. However, I strongly recommend Google Chrome.

#### Installing Google Chrome

Install [Google Chrome](https://www.google.com/chrome/) if you do not have one yet. We can write small JavaScript code on the browser console, but we do not use the browser console to develop applications.

![Google Chrome](/images/google_chrome.png)

#### Opening Google Chrome Console

You can open Google Chrome console either by clicking three dots at the top right corner of the browser, selecting _More tools -> Developer tools_ or using a keyboard shortcut. I prefer using shortcuts.

![Opening chrome](/images/opening_developer_tool.png)

To open the Chrome console using a keyboard shortcut.

```sh
Mac
Command+Option+J

Windows/Linux:
Ctl+Shift+J
```

![Opening console](/images/opening_chrome_console_shortcut.png)

After you open the Google Chrome console, try to explore the marked buttons. We will spend most of the time on the Console. The Console is the place where your JavaScript code goes. The Google Console V8 engine changes your JavaScript code to machine code.
Let us write a JavaScript code on the Google Chrome console:

![write code on console](/images/js_code_on_chrome_console.png)

#### Writing Code on Browser Console

We can write any JavaScript code on the Google console or any browser console. However, for this challenge, we only focus on Google Chrome console. Open the console using:

```sh
Mac
Command+Option+I

Windows:
Ctl+Shift+I
```

##### Console.log

To write our first JavaScript code, we used a built-in function **console.log()**. We passed an argument as input data, and the function displays the output. We passed `'Hello, World'` as input data or argument in the console.log() function.

```js
console.log('Hello, World!')
```

##### Console.log with Multiple Arguments

The **`console.log()`** function can take multiple parameters separated by commas. The syntax looks like as follows:**`console.log(param1, param2, param3)`**

![console log multiple arguments](/images/console_log_multipl_arguments.png)

```js
console.log('Hello', 'World', '!')
console.log('HAPPY', 'NEW', 'YEAR', 2020)
console.log('Welcome', 'to', 30, 'Days', 'Of', 'JavaScript')
```

As you can see from the snippet code above, _`console.log()`_ can take multiple arguments.

Congratulations! You wrote your first JavaScript code using _`console.log()`_.

##### Comments

We can add comments to our code. Comments are very important to make code more readable and to leave remarks in our code. JavaScript does not execute the comment part of our code. In JavaScript, any text line starting with // in JavaScript is a comment, and anything enclosed like this `//` is also a comment.

**Example: Single Line Comment**

```js
// This is the first comment  
// This is the second comment  
// I am a single line comment
```

**Example: Multiline Comment**

```js
/*
This is a multiline comment  
 Multiline comments can take multiple lines  
 JavaScript is the language of the web  
 */
```

##### Syntax

Programming languages are similar to human languages. English or many other language uses words, phrases, sentences, compound sentences and other more to convey a meaningful message. The English meaning of syntax is _the arrangement of words and phrases to create well-formed sentences in a language_. The technical definition of syntax is the structure of statements in a computer language. Programming languages have syntax. JavaScript is a programming language and like other programming languages it has its own syntax. If we do not write a syntax that JavaScript understands, it will raise different types of errors. We will explore different kinds of JavaScript errors later. For now, let us see syntax errors.

![Error](/images/raising_syntax_error.png)

I made a deliberate mistake. As a result, the console raises syntax errors. Actually, the syntax is very informative. It informs what type of mistake was made. By reading the error feedback guideline, we can correct the syntax and fix the problem. The process of identifying and removing errors from a program is called debugging. Let us fix the errors:

```js
console.log('Hello, World!')
console.log('Hello, World!')
```

So far, we saw how to display text using the _`console.log()`_. If we are printing text or string using _`console.log()`_, the text has to be inside the single quotes, double quotes, or a backtick.
**Example:**

```js
console.log('Hello, World!')
console.log("Hello, World!")
console.log(`Hello, World!`)
```

#### Arithmetics

Now, let us practice more writing JavaScript codes using _`console.log()`_ on Google Chrome console for number data types.
In addition to the text, we can also do mathematical calculations using JavaScript. Let us do the following simple calculations.
It is possible to write JavaScript code on Google Chrome console can directly without the **_`console.log()`_** function. However, it is included in this introduction because most of this challenge would be taking place in a text editor where the usage of the function would be mandatory. You can play around directly with instructions on the console.

![Arithmetic](/images/arithmetic.png)

```js
console.log(2 + 3) // Addition
console.log(3 - 2) // Subtraction
console.log(2 * 3) // Multiplication
console.log(3 / 2) // Division
console.log(3 % 2) // Modulus - finding remainder
console.log(3 ** 2) // Exponentiation 3 ** 2 == 3 * 3
```

### Code Editor

We can write our codes on the browser console, but it won't be for bigger projects. In a real working environment, developers use different code editors to write their codes. In this 30 days of JavaScript challenge, we will be using Visual Studio Code.

#### Installing Visual Studio Code

Visual Studio Code is a very popular open-source text editor. I would recommend to [download Visual Studio Code](https://code.visualstudio.com/), but if you are in favor of other editors, feel free to follow with what you have.

![Vscode](/images/vscode.png)

If you installed Visual Studio Code, let us start using it.

#### How to Use Visual Studio Code

Open the Visual Studio Code by double-clicking its icon. When you open it, you will get this kind of interface. Try to interact with the labeled icons.

![Vscode ui](/images/vscode_ui.png)

![Vscode add project](/images/adding_project_to_vscode.png)

![Vscode open project](.images/opening_project_on_vscode.png)

![script file](/images/scripts_on_vscode.png)

![Installing Live Server](/images/vsc_live_server.png)

![running script](/images/running_script.png)

![coding running](/images/launched_on_new_tab.png)

## Adding JavaScript to a Web Page

JavaScript can be added to a web page in three different ways:

- **_Inline script_**
- **_Internal script_**
- **_External script_**
- **_Multiple External scripts_**

The following sections show different ways of adding JavaScript code to your web page.

### Inline Script

Create a project folder on your desktop or in any location, name it 30DaysOfJS and create an **_`index.html`_** file in the project folder. Then paste the following code and open it in a browser, for example [Chrome](https://www.google.com/chrome/).

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>30DaysOfScript:Inline Script</title>
  </head>
  <body>
    <button onclick="alert('Welcome to 30DaysOfJavaScript!')">Click Me</button>
  </body>
</html>
```

Now, you just wrote your first inline script. We can create a pop up alert message using the _`alert()`_ built-in function.

### Internal Script

The internal script can be written in the _`head`_ or the _`body`_, but it is preferred to put it on the body of the HTML document.
First, let us write on the head part of the page.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>30DaysOfScript:Internal Script</title>
    <script>
      console.log('Welcome to 30DaysOfJavaScript')
    </script>
  </head>
  <body></body>
</html>
```

This is how we write an internal script most of the time. Writing the JavaScript code in the body section is the most preferred option. Open the browser console to see the output from the `console.log()`.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>30DaysOfScript:Internal Script</title>
  </head>
  <body>
    <button onclick="alert('Welcome to 30DaysOfJavaScript!');">Click Me</button>
    <script>
      console.log('Welcome to 30DaysOfJavaScript')
    </script>
  </body>
</html>
```

Open the browser console to see the output from the `console.log()`.

![js code from vscode](/images/js_code_vscode.png)

### External Script

Similar to the internal script, the external script link can be on the header or body, but it is preferred to put it in the body.
First, we should create an external JavaScript file with .js extension. All files ending with .js extension are JavaScript files. Create a file named introduction.js inside your project directory and write the following code and link this .js file at the bottom of the body.

```js
console.log('Welcome to 30DaysOfJavaScript')
```

External scripts in the _head_:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>30DaysOfJavaScript:External script</title>
    <script src="introduction.js"></script>
  </head>
  <body></body>
</html>
```

External scripts in the _body_:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>30DaysOfJavaScript:External script</title>
  </head>
  <body>
    <!-- JavaScript external link could be in the header or in the body --> 
    <!-- Before the closing tag of the body is the recommended place to put the external JavaScript script -->
    <script src="introduction.js"></script>
  </body>
</html>
```

Open the browser console to see the output of the `console.log()`.

### Multiple External Scripts

We can also link multiple external JavaScript files to a web page.
Create a `helloworld.js` file inside the 30DaysOfJS folder and write the following code.

```js
console.log('Hello, World!')
```

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Multiple External Scripts</title>
  </head>
  <body>
    <script src="./helloworld.js"></script>
    <script src="./introduction.js"></script>
  </body>
</html>
```

_Your main.js file should be below all other scripts_. It is very important to remember this.

![Multiple Script](/images/multiple_script.png)