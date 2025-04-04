# JavaScript Functions

A function in JavaScript is a reusable block of code designed to perform a specific task. Functions help break large programs into smaller, manageable parts.

## Declaring a Function
Functions are defined using the `function` keyword.

### Syntax:
```js
function functionName(param1, param2) {
  // Code to execute
  return result; // Optional
}
```
### Example:
```js
function greet(name) {
  console.log("Hello, " + name + "!");
}
greet("Alice");
```
#### Output:
```
Hello, Alice!
```

## Function Expressions
Functions can also be stored in variables.

```js
const multiply = function (a, b) {
  return a * b;
};
let result = multiply(4, 8);
console.log(result);
```
#### Output:
```
32
```

## JavaScript Function Methods
- **apply()** - Calls a function with `this` value and arguments as an array.
- **bind()** - Creates a new function.
- **call()** - Calls a function with `this` value and arguments.
- **toString()** - Returns function code as a string.

## Types of JavaScript Functions

### Arrow Functions
Introduced in ES6, arrow functions provide a concise syntax.
```js
const add = (a, b) => a + b;
console.log(add(5, 3));
```

### Callback Functions
A function passed as a parameter to another function.
```js
function showData(name) {
  console.log("Hello, " + name);
}
function getData(callback) {
  let name = "Rohit";
  callback(name);
}
getData(showData);
```

### Anonymous Functions
- Functions without a name.
- in this case if we access function before creation the ive us error.
```js
let x = function () {
  console.log("Anonymous function");
};
x();
```

### Immediately Invoked Function Expression (IIFE)
Executed immediately after definition.
```js
(function() {
  console.log("IIFE executed");
})();
```

### Nested Functions
A function inside another function.
```js
function outer(a) {
  function inner(b) {
    return a + b;
  }
  return inner;
}
const addTen = outer(10);
console.log(addTen(5));
```
#### Output:
```
15
```

## Advantages of Functions
- **Reusability**: Write once, use multiple times.
- **Modularity**: Organizes code into logical sections.
- **Readability**: Makes code easier to understand.
- **Maintenance**: Easier to update without affecting the rest of the program.
- **Debugging**: Isolates errors to specific functions.

This guide provides an overview of JavaScript functions with simple examples.
