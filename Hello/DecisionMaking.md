# Decision Making in JavaScript

## Introduction
Decision making is a crucial aspect of programming that allows developers to execute different blocks of code based on conditions. JavaScript provides several constructs for implementing decision-making logic.

## Conditional Statements
JavaScript supports several conditional statements:

### 1. `if` Statement
The `if` statement evaluates a condition and executes a block of code if the condition is `true`.
```javascript
let age = 18;
if (age >= 18) {
    console.log("You are eligible to vote.");
}
```

### 2. `if-else` Statement
The `if-else` statement provides an alternative block of code to execute if the condition is `false`.
```javascript
let age = 16;
if (age >= 18) {
    console.log("You can vote.");
} else {
    console.log("You are not eligible to vote.");
}
```

### 3. `if-else if-else` Ladder
Used when there are multiple conditions to check.
```javascript
let score = 85;
if (score >= 90) {
    console.log("Grade: A");
} else if (score >= 80) {
    console.log("Grade: B");
} else if (score >= 70) {
    console.log("Grade: C");
} else {
    console.log("Fail");
}
```

### 4. `switch` Statement
The `switch` statement evaluates an expression and executes the corresponding `case`.
```javascript
let day = "Monday";
switch (day) {
    case "Monday":
        console.log("Start of the work week.");
        break;
    case "Friday":
        console.log("Weekend is near.");
        break;
    default:
        console.log("Regular day.");
}
```

## Ternary Operator
A shorthand for `if-else` statements.
```javascript
let age = 20;
let message = (age >= 18) ? "Eligible to vote" : "Not eligible to vote";
console.log(message);
```

## Logical Operators in Decision Making
JavaScript provides logical operators that help in combining multiple conditions:
- `&&` (AND) operator: Both conditions must be true.
- `||` (OR) operator: At least one condition must be true.
- `!` (NOT) operator: Reverses the condition.

Example:
```javascript
let age = 20;
let hasID = true;
if (age >= 18 && hasID) {
    console.log("You can enter the club.");
} else {
    console.log("Access denied.");
}
```

## Conclusion
Decision-making statements in JavaScript allow developers to control program flow efficiently. By using `if`, `if-else`, `switch`, and the ternary operator, JavaScript enables flexible decision logic for applications.

