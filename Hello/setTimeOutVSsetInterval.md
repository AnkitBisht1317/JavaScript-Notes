# setTimeout()
- setTimeout executes a function once after a specified delay (in milliseconds).
- setTimeout(function, delayInMilliseconds);
```javascript
console.log("Start");
setTimeout(function () {
  console.log("Executed after 2 seconds");
}, 2000); // 2000ms = 2 seconds
console.log("End");
```

# setInterval()
- setInterval executes a function repeatedly at a fixed time interval.
- setInterval(function, intervalInMilliseconds);

```javascript
setInterval(function () {
  console.log("Repeats every 1 second");
}, 1000);
```

### Where Do We Use setTimeout and setInterval?
- Delaying actions	setTimeout	Wait before showing a message, popup, etc.
- Animations and effects	setTimeout, setInterval	Trigger animations after delay or in loops.
- Auto-logout timers	setTimeout	Log user out after inactivity.
- Live clocks or countdowns	setInterval	Update time every second.
- Polling or fetching data	setInterval	Call API again and again at intervals.
- Slideshow or carousel timer	setInterval	Change image every few seconds.
