# Comparison Operators in JavaScript
JavaScript provides several comparison operators to compare values. These operators return a boolean (true or false) based on the comparison.

### List of Comparison Operators

- ==	Equal to (loose equality, performs type conversion)	
- ===	Strictly equal (checks both value and type)	
- !=	Not equal (loose inequality)	
- !==	Strictly not equal (value or type mismatch)	
- >	Greater than	
- <	Less than	
- >=	Greater than or equal to
- <=	Less than or equal to

```javascript
const userAge1 = 21;
const userAge2 = 24;

console.log(userAge1 > userAge2);  // false
console.log(userAge1 < userAge2);  // true
console.log(userAge1 == '21');     // true (because of type coercion)
console.log(userAge1 === '21');    // false (strict comparison)
console.log(userAge1 !== 24);      // true
```
## Difference Between == and === in JavaScript

#### == (Equality Operator)
Performs type conversion (coercion) before comparing values.
If the types don’t match, JavaScript tries to convert one type to match the other.
```javascript
console.log(5 == '5');  // true (string '5' is converted to a number)
console.log(0 == false); // true (false is converted to 0)
console.log(null == undefined); // true (both are considered loosely equal)
```
#### === (Strict Equality Operator)
Does not perform type conversion.
Both the value and type must be the same to return true.
```javascript
console.log(5 === '5');  // false (number !== string)
console.log(0 === false); // false (boolean !== number)
console.log(null === undefined); // false (different types)
```
