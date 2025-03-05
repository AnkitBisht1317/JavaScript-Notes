# Mathematical Operators
JavaScript provides various mathematical operators to perform arithmetic operations.

## Operator	Description	Example	Result
- Addition	5 + 3	8
- Subtraction	5 - 3	2
- Multiplication	5 * 3	15
- Division	5 / 2	2.5
- Remainder (Modulo)	5 % 2	1
- Exponentiation (Power)	5 ** 2	25
 	
## Math Object in JavaScript
JavaScript provides a built-in Math object that includes properties and methods for mathematical calculations.

## Properties of Math Object
These are commonly used mathematical constants:

- Math.PI → The value of π (3.141592653589793).
- Math.SQRT2 → The square root of 2 (~1.414).
- Math.E → Euler’s number (~2.718).

## Method	Description	Example	Result
- Math.sqrt(x)	Returns the square root of x.	Math.sqrt(25)	5
- Math.pow(x, y)	Returns x raised to the power of y.	Math.pow(2, 3)	8
- Math.floor(x)	Rounds x down to the nearest integer.	Math.floor(2.9)	2
- Math.ceil(x)	Rounds x up to the nearest integer.	Math.ceil(2.1)	3
- Math.round(x)	Rounds x to the nearest integer.	Math.round(2.5)	3
- Math.random()	Returns a random number between 0 and 1.	Math.random()	0.XXX

### Special Cases in JavaScript Math
Division by zero (/ 0) results in Infinity.
console.log(8 / 0); // Output: Infinity
console.log(-8 / 0); // Output: -Infinity
```
Example: Calculating the Area of a Rectangle
This program prompts the user for the width and height of a rectangle, then calculates and displays the area.

const width = +prompt("Please Enter Rectangle Width");
const height = +prompt("Please Enter Rectangle Height");

console.log("Area:", width * height);
document.write(`Rectangle Area: ${width * height}`);
Example Output:
Input: width = 5, height = 10
Output: Rectangle Area: 50
```
