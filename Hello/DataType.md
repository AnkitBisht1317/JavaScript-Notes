# Data Types in JavaScript

JavaScript provides different data types to hold different types of values. There are two major categories:

## Primitive Data Types
These are immutable and stored directly in memory.

1. **String** - Represents textual data.
   ```js
   let name = "John Doe";
   ```
2. **Number** - Represents both integers and floating-point numbers.
   ```js
   let age = 25;
   let price = 99.99;
   ```
3. **Boolean** - Represents `true` or `false` values.
   ```js
   let isAvailable = true;
   ```
4. **Undefined** - A variable that has been declared but not assigned a value.
   ```js
   let value;
   console.log(value); // undefined
   ```
5. **Null** - Represents an intentional absence of a value.
   ```js
   let data = null;
   ```
6. **Symbol (ES6)** - Represents a unique and immutable identifier.
   ```js
   let sym = Symbol("unique");
   ```
7. **BigInt (ES11)** - Used for large integer values beyond `Number.MAX_SAFE_INTEGER`.
   ```js
   let bigNumber = 123456789012345678901234567890n;
   ```

## Non-Primitive (Reference) Data Types
These are mutable and stored as references in memory.

1. **Object** - Collection of key-value pairs.
   ```js
   let person = {
       name: "Alice",
       age: 30
   };
   ```
2. **Array** - Ordered list of values.
   ```js
   let numbers = [1, 2, 3, 4, 5];
   ```
3. **Function** - A block of reusable code.
   ```js
   function greet() {
       return "Hello!";
   }
   ```

## Type Checking
Use `typeof` to check the data type.
```js
console.log(typeof 42); // "number"
console.log(typeof "hello"); // "string"
console.log(typeof {}); // "object"
console.log(typeof []); // "object" (arrays are special objects)
console.log(typeof null); // "object" (known JavaScript quirk)
console.log(typeof function(){}); // "function"
```

## Summary Table
| Data Type | Example |
|-----------|---------|
| String | `"Hello"` |
| Number | `42`, `3.14` |
| Boolean | `true`, `false` |
| Undefined | `undefined` |
| Null | `null` |
| Symbol | `Symbol('id')` |
| BigInt | `12345678901234567890n` |
| Object | `{ key: "value" }` |
| Array | `[1, 2, 3]` |
| Function | `function() {}` |

Understanding data types helps in writing efficient and error-free code.
