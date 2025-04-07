#  Global vs  Local Scope in JavaScript
- In JavaScript, scope refers to the current context of execution in which values and expressions are visible or can be referenced. There are mainly two types:
## Global Scope
- Variables declared using var outside any function are attached to the window object (in browsers), hence they are global.
- Functions declared in the global context are also accessible globally and attached to the window.
- Variables declared using let or const in the global scope are not attached to the window object, but they are still globally available within the script (Script Scope).

##  Local Scope
- Variables declared inside a function using var, let, or const are only accessible within that function.
- These variables are not accessible outside the function – this is known as function scope or block scope.

```javascript
  const username = 'Ankit';
  let age = 25;
  var a = 50;

  function add() {
    const x = 5;
    const y = 10;
    console.log(x + y);  // Output: 15
  }

  add();

  console.log('Program Executed');
```
##  Global Scope:
Window Object (Browser Global)	        Script Scope
a = 50	                                username = 'Ankit'
add = function()	                      age = 25
- Note: Only var and function declarations are attached to the window object. let and const are not.

 ## ✅ Local Scope (Inside add() function):
Variable	        Scope
x = 5	            Local
y = 10	           Local
- These are accessible only inside the add() function and not from the outside.

