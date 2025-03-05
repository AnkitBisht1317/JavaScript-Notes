## String Methods and Properties in JavaScript
Introduction
Before diving into string methods and properties, it's important to know that strings are indexed. This means we can access individual characters in a string using their index.

## String Property
JavaScript strings have only one property:

length → Returns the length of a string.
const text = "Hello";
console.log(text.length); // Output: 5


## String Methods
### Methods Without Arguments
These methods do not require arguments:

toUpperCase() → Converts string to uppercase.
toLowerCase() → Converts string to lowercase.
trim() → Removes whitespace from both ends.
trimStart() → Removes whitespace from the beginning.
trimEnd() → Removes whitespace from the end.
Methods With Arguments


### These methods require arguments to function:

includes(searchString) → Checks if a string contains a substring.
indexOf(searchString) → Returns the first occurrence index of a substring.
replace(old, new) → Replaces the first occurrence of a substring.
replaceAll(old, new) → Replaces all occurrences of a substring.
concat(string1, string2, ...) → Joins strings together.
padStart(targetLength, padString) → Pads a string at the start.
padEnd(targetLength, padString) → Pads a string at the end.
charAt(index) → Returns the character at the given index.
charCodeAt(index) → Returns the Unicode of the character at the index.
split(separator) → Splits a string into an array based on a separator.

  
### Basic String Operations

const message = 'Hello World!';
console.log(message.toUpperCase()); // "HELLO WORLD!"
console.log(message.toLowerCase()); // "hello world!"

const text = '     Hi, I am Anurag.     ';
console.log(text.trim()); // "Hi, I am Anurag."


const finalMessage = text.trim();
console.log(finalMessage.replace('Hi', 'Hello')); // "Hello, I am Anurag."

const lastFourDigits = '9996';
const maskedAccountNumber = lastFourDigits.padStart(16, '*');

console.log(maskedAccountNumber); // "************9996"
const bankBalance = 9873;
console.log(`My account number ends in ${lastFourDigits}.`); 
console.log(`I have ₹${bankBalance} in my account.`);

console.log('Last four digits of my account number are'.concat(' ', lastFourDigits));
