# Class Expressions
A class expression is another way to define a class. Class expressions can be named or unnamed. The name given to a named class expression is local to the class's body. However, it can be accessed via the [name](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/name) property.
```js
// unnamed
let Rectangle = class {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
};
console.log(Rectangle.name);
// output: "Rectangle"

// named
Rectangle = class Rectangle2 {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
};
console.log(Rectangle.name);
// output: "Rectangle2"
```

Note: Class expressions must be declared before they can be used (they are subject to the same hoisting restrictions as described in the [class declarations](#class-declaration) section).

# Class Declaration
One way to define a class is using a class declaration. To declare a class, you use the class keyword with the name of the `class` ("Rectangle" here).
```js
class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
}
```



