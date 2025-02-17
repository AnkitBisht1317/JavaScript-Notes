In JavaScript, `var`, `let`, and `const` are used to declare variables, but they differ in terms of scope, hoisting, and mutability. Here's a breakdown of each:

## 1. var
- **Scope**: Function-scoped (or globally scoped if declared outside a function).
- **Hoisting**: Variables declared with `var` are hoisted to the top of their scope and initialized with `undefined`.
- **Reassignment**: Can be reassigned and updated.
- **Redeclaration**: Can be redeclared within the same scope.

### Example:
```javascript
var x = 10;
if (true) {
  var x = 20; // Same variable, reassigned
}
console.log(x); // Output: 20
```

## 2. let
- **Scope**: Block-scoped (limited to the block in which it is declared, e.g., inside `{}`).
- **Hoisting**: Variables declared with `let` are hoisted but not initialized (temporal dead zone until declaration).
- **Reassignment**: Can be reassigned and updated.
- **Redeclaration**: Cannot be redeclared within the same scope.

### Example:
```javascript
let y = 10;
if (true) {
  let y = 20; // Different variable, block-scoped
}
console.log(y); // Output: 10
```

## 3. const
- **Scope**: Block-scoped (like `let`).
- **Hoisting**: Variables declared with `const` are hoisted but not initialized (temporal dead zone until declaration).
- **Reassignment**: Cannot be reassigned or updated (immutable binding).
- **Redeclaration**: Cannot be redeclared within the same scope.

### Example:
```javascript
const z = 10;
if (true) {
  const z = 20; // Different variable, block-scoped
}
console.log(z); // Output: 10
```

## Key Differences:
| Feature      | `var` | `let` | `const` |
|-------------|-------|-------|--------|
| **Scope**   | Function or global | Block-scoped | Block-scoped |
| **Hoisting** | Hoisted (initialized as `undefined`) | Hoisted (not initialized) | Hoisted (not initialized) |
| **Reassignment** | Allowed | Allowed | Not allowed |
| **Redeclaration** | Allowed | Not allowed | Not allowed |
| **Use Case** | Legacy code (avoid in modern JS) | Variables that need reassignment | Constants or immutable values |

## When to Use:
- **Use `const`** by default for variables that don’t need reassignment.
- **Use `let`** for variables that need to be reassigned.
- **Avoid `var`** in modern JavaScript due to its function-scoping and hoisting behavior, which can lead to bugs.

### Example Summary:
```javascript
var a = 1; // Avoid using var
let b = 2; // Use for reassignable variables
const c = 3; // Use for constants

b = 4; // Valid
// c = 5; // Error: Assignment to constant variable
```

