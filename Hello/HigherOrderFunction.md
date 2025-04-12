# Higher-Order Functions in JavaScript
- A higher-order function is a function that either:
- Takes one or more functions as arguments, or
- Returns a function as its result

```javascript
// Higher-order function that takes a function as an argument
function greet(name, greetingFunction) {
  return greetingFunction(name);
}

// Functions to pass as arguments
function sayHello(name) {
  return `Hello, ${name}!`;
}

function sayGoodbye(name) {
  return `Goodbye, ${name}!`;
}

// Using the higher-order function
console.log(greet('Alice', sayHello));    // "Hello, Alice!"
console.log(greet('Bob', sayGoodbye));    // "Goodbye, Bob!"
```
