## JavaScript Execution System: The Key Players
- Call Stack	= Runs functions one at a time (synchronous code).
- Web APIs	= Handles async tasks like timers, HTTP requests, etc.
- Callback Queue =	Stores async callbacks when they are ready to run.
- Event Loop	= Moves callbacks from the queue to the stack when it's empty.

# Simple Flow:
- JS runs code line by line in the Call Stack.
- If it sees something like setTimeout, it sends it to Web APIs.
- After the time finishes, the callback goes to the Callback Queue.
- The Event Loop checks if the Call Stack is empty, then moves the callback from the queue to the stack to be executed.

```javascript
console.log("1");
setTimeout(() => {
  console.log("2");
}, 2000);
console.log("3");
```
Output
1
3
2
