# HOISTING
- In javascript function declarations are hoisting , meaning you can call them before they are define in the code.

 ## How Hoisting Works : 
 ### A. Variable Hoisting
 #### var Declarations:
- Variables declared with var are hoisted to the top of their scope and initialized with undefined.
```javascript
console.log(x); // undefined (not ReferenceError)
var x = 5;
```
#### let and const Declarations (Temporal Dead Zone - TDZ):
- Variables declared with let and const are hoisted but not initialized (unlike var).
- Accessing them before declaration results in a ReferenceError.
```javascript
console.log(y); // ReferenceError: Cannot access 'y' before initialization
let y = 10;
```

### B. Function Hoisting : 
#### Function Declarations:
- Entire function definitions are hoisted (name + body).
- Can be called before declaration.
```javascript
greet(); // "Hello!"
function greet() {
  console.log("Hello!");
}
```
#### Function Expressions:
- Only the variable declaration is hoisted (if using var), not the function itself.
```javascript
console.log(funcExpr); // undefined (if var)
var funcExpr = function() {
  console.log("Function Expression");
};
```
```javascript
greet(); // ❌ ReferenceError

let greet = function () {
  console.log("Hi!");
};
```
