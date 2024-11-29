# JavaScript Event Handling

JavaScript, being a sequential programming language, executes most of its events in the order they occur. Event handling is key to creating interactive web applications.

---

### Key Concepts:

#### 1. Basic Event Handling

Events in JavaScript can be handled using two main approaches:

1. **Assigning an Event Directly (Older Method)**:
   - Example: `element.onclick`.

2. **Using `addEventListener` (Modern Method, Preferred)**:
   - Example: `element.addEventListener('event', handler)`.

#### Examples:
```javascript
// Older Method
function approachOnclick() {
    document.getElementById("owl").onclick = function() {
        console.log("Owl Clicked");
    }
}

// Modern Method
function EventListenerAppr() {
    document.getElementById("owl").addEventListener("click", function(ev) {
        console.log("Owl Clicked");
    });
}

```
#### 2. Event Object in JavaScript

- Whenever an event occurs in JavaScript, an **event object** is created containing detailed information about the event. 

- You can access this object as a parameter in your event handler.

##### Key Properties to Explore:

- **General Info** :  
**`type`**,**`timeStamp`**,**`defaultPrevented`**.
- **Target Information** : **`target`**,**`toElement`**,**`srcElement`**,**`currentTarget`**

- **Coordinates** **
**`clientX`**,**`clientY`**,**`screenX`**,**`screenY`**.

- **Modifiers**
**`altKey`**,**`ctrlKey`**,**`shiftKey`**,**`keyCode`**

#### Example
```javascript
function eventObject() {
    document.getElementById("owl").addEventListener("click", function(event) {
        console.log(event); // Logs the event object
    });
}
```

#### 3. Event Propagation :
Events propagate through two main phases:
- **Event Bubbling** (Default): The event moves from the innermost element to the outermost (**`Bottom to Top`**).
- **Event Capturing**: The event moves from the outermost element to the innermost (**`Top to Bottom`**).

#### Managing Propagation
- **`stopPropagation()`**: Stops further propagation of the event in the bubbling or capturing phase.
- **`addEventListener` third parameter**:
  - `true` for capturing phase.
  - `false` (default) for bubbling phase.

## Example

```javascript
function eventPropagation() {
    // Bubbling Phase
    document.getElementById("images").addEventListener("click", function(event) {
        console.log("Clicked inside the ul");
    }, false);

    document.getElementById("owl").addEventListener("click", function(event) {
        console.log("Owl Clicked!");
        event.stopPropagation(); // Prevents event from propagating further
    }, false);

    // Capturing Phase
    document.getElementById("images").addEventListener("click", function(event) {
        console.log("Clicked inside the ul");
    }, true);

    document.getElementById("owl").addEventListener("click", function(event) {
        console.log("Owl Clicked!");
    }, true);
}
```

#### 4.  Prevent Default Behavior

- Some elements (e.g., `<a>` tags) have default behaviors.
- Use `event.preventDefault()` to cancel those behaviors.

##### Example:

```JavaScript
document.getElementById("google").addEventListener("click", function(event) {
    event.preventDefault(); // Prevents the link from navigating
    console.log("Google Clicked");
});
```

#### 5. Dynamic Removal of Elements

- You can dynamically remove elements from the DOM by identifying them through event delegation.
- Use `event.target` to identify the clicked element and `parentNode.remove()` to remove it.

##### Example:

```JavaScript
function removeImages() {
    document.getElementById("images").addEventListener("click", function(event) {
        console.log(event.target.parentNode);
        console.log(event.target.tagName);
        if (event.target.tagName === "IMG") {
            let removeIt = event.target.parentNode;
            removeIt.remove(); // Removes the parent node
        }
    });
}
```

### Key Takeaways

- Use `addEventListener` for modern, scalable event handling.
- Understand the event object to access detailed event properties.
- Manage event propagation using bubbling and capturing, and control flow with `stopPropagation`.
- Use `preventDefault()` to cancel default browser behaviors.
- For dynamic changes, such as removing elements, leverage event delegation and `event.target`.

These concepts are fundamental for effectively handling user interactions in JavaScript.