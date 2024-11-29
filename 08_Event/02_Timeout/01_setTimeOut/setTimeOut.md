#  setTimeout

### Definition
`setTimeout` is a JavaScript function that executes a piece of code after a specified delay in milliseconds. It is often used to delay actions or to execute functions asynchronously after a set period. The `setTimeout()` function takes two arguments:

1. A function to be executed.
2. A time in milliseconds that specifies the delay before the function is executed.

The `clearTimeout()` function can be used to stop a timeout that was previously set with `setTimeout()` before it executes.

#### Code Explanation

##### 1. Basic Timeout with Anonymous Function:

```javascript
setTimeout(function(){
    console.log("Ravindra");
}, 5000);
```
This will log "Ravindra" to the console after 5 seconds.

##### 2. Timeout with Named Function:
``` javaScript
const sayGaurav = function() {
    console.log("Gaurav");
};
setTimeout(sayGaurav, 2000);
```
This will log "Gaurav" to the console after 2 seconds. It demonstrates passing a named function to `setTimeout()`.

##### 3. Changing Text after Delay:
```javascript
const changeText = function() {
    document.querySelector("h1").innerHTML = "JavaScript Learning";
};
const changeMe = setTimeout(changeText, 2000);
```
This code changes the text of the `<h1>` element to "JavaScript Learning" after 2 seconds.

##### 4. Stopping the Timeout:

```javascript
document.querySelector("#stop").addEventListener("click", function(){
    clearTimeout(changeMe);
    console.log("Stopped");
});
```
If the user clicks an element with the ID `stop`, it will cancel the previously set timeout (change the `<h1>` text) and log "Stopped" to the console.

#### Key Concepts and Notes

#### `setTimeout()`:
- Delays the execution of a function by the specified number of milliseconds.
- Executes only once after the delay period.

#### `clearTimeout()`:
- Used to cancel a previously set `setTimeout()`.
- Prevents the scheduled function from executing if the timeout has not yet elapsed.

##### Anonymous Functions:
- Functions can be defined inline within `setTimeout()` calls, making the code more concise.

##### Handling Timeouts in the DOM:
- You can interact with the DOM (like changing text or other properties) after a delay.
- You can also use `clearTimeout()` in conjunction with DOM events (such as a button click) to cancel actions.

#### Summary
- `setTimeout()` schedules a function to run after a delay.
- `clearTimeout()` allows you to cancel the scheduled function before it runs.
- Useful for delaying actions or cancelling functions based on user interactions or conditions.
- This method is commonly used for simple timed delays or animations, or in cases where you want to delay a function call without blocking the rest of the code.


### HTML
```javascript
<body style="background-color: #000000; color: #ffff;">
    <h1>SetTimeOut & SetInterval</h1>
    <button id="stop">Stop</button>

    <script src="script.js"></script>
</body>
```