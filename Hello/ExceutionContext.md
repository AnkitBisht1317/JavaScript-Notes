## Question - What is Execution Context?
- Execution Context is the environment where JavaScript code is executed. It's a conceptual environment that contains all the information necessary to execute code, including variable and function declarations, scope chain, and the value of this.

### Types of Execution Context
#### 1.Global Execution Context (GEC)
- Created when the JavaScript engine first starts executing your code
- There's only one GEC per program
- In browsers, the global object is window
-this refers to the global object (window in browsers)

#### 2.Function Execution Context (FEC)
- Created whenever a function is invoked/called
- Each function call creates its own execution context
- Has access to its own variables and the outer scope's variables

#### 3.Eval Execution Context
- Created when code is executed inside an eval() function
- Rarely used and generally discouraged

![Image](https://github.com/user-attachments/assets/97f2eb56-4c08-4bf9-a5a7-ccd9367baf02)


