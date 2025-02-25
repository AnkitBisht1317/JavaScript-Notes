JavaScript Code Execution Process

Variable Declaration and Initialization

In JavaScript, variables can be declared using var, let, and const. Below is an example of variable declarations:

var firstName = "Ankit";
let lastName = "Bisht";
let age = 22;
const yearOfBirth = 2002;

Execution Process in JavaScript

JavaScript code execution happens in two main phases:

Step 1: Memory Creation Phase

During this phase, JavaScript allocates memory for variables and functions before executing the actual code.
All variables declared using var, let, and const are assigned an initial value of undefined.
Their types are also set as undefined until they are assigned actual values.

Example Memory Allocation:

firstName → undefined  
lastName  → undefined  
age       → undefined  
yearOfBirth → undefined  

Step 2: Code Execution Phase

In this phase, the JavaScript engine assigns actual values to the variables and executes the code line by line.

Example After Execution:

firstName → "Ankit"  
lastName  → "Bisht"  
age       → 22  
yearOfBirth → 2002  

Defer Attribute in <script> Tag

If we add the defer attribute inside a <script> tag:

<script src="script.js" defer></script>

It ensures that the entire HTML content is loaded first before JavaScript execution begins.

