# Dialog Box
In web development, alert, confirm, and prompt boxes are JavaScript pop-up dialog boxes used to interact with users. They are simple and built into browsers, making them easy to use for basic user interactions. Below is a detailed explanation of each, along with their use cases and how to implement them in HTML using JavaScript.

## 1. Alert Box
#### Purpose: Displays a message to the user and waits for the user to acknowledge it by clicking "OK."
#### Use Case: Used to show important information, warnings, or notifications that require user attention.
```html
html
Copy
<!DOCTYPE html>
<html>
<head>
    <title>Alert Example</title>
</head>
<body>
    <button onclick="showAlert()">Click Me</button>
    <script>
        function showAlert() {
            alert("This is an alert box!");
        }
    </script>
</body>
</html>
```

## 2. Confirm Box
#### Purpose: Displays a message with two buttons: "OK" and "Cancel." It returns true if the user clicks "OK" and false if the user clicks "Cancel."
#### Use Case: Used to ask the user for confirmation before performing an action (e.g., deleting a file, submitting a form).
```html
html
Copy
<!DOCTYPE html>
<html>
<head>
    <title>Confirm Example</title>
</head>
<body>
    <button onclick="showConfirm()">Delete File</button>
    <script>
        function showConfirm() {
            const result = confirm("Are you sure you want to delete this file?");
            if (result) {
                alert("File deleted!");
            } else {
                alert("Deletion canceled.");
            }
        }
    </script>
</body>
</html>
```

## 3. Prompt Box
#### Purpose: Displays a message and a text input field. It returns the user's input as a string if the user clicks "OK" or null if the user clicks "Cancel."
#### Use Case: Used to get input from the user (e.g., asking for a name, age, or other information).
```html
html
Copy
<!DOCTYPE html>
<html>
<head>
    <title>Prompt Example</title>
</head>
<body>
    <button onclick="showPrompt()">Enter Your Name</button>
    <script>
        function showPrompt() {
            const name = prompt("Please enter your name:", "John Doe");
            if (name) {
                alert("Hello, " + name + "!");
            } else {
                alert("You didn't enter a name.");
            }
        }
    </script>
</body>
</html>
```
