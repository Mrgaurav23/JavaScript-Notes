## Definitions
#### 1. Functions as Objects in JavaScript
- In JavaScript, functions are first-class objects. This means they can:
    - Be assigned to variables.
    - Have properties and methods.
    - Be passed as arguments or returned from other functions.
##### Example:
```javascript
function multiplyBY5(num) {
    return num * 5;
}
multiplyBY5.power = 2; // Adding a property to the function.
```
#### 2. Function Prototype
- Every JavaScript function has a **`prototype`** property, which is an object used to attach shared methods or properties for instances created by the function.
- The **`prototype`** is especially important for constructor functions, as it allows all instances to share the same methods or properties.


#### 3. Constructor Function
- A Constructor Function is used to create objects with specific properties and methods.
- Instances created with a constructor function inherit shared methods and properties through the function's prototype.
##### Example:
```javascript
function createUser(userName, score) {
    this.userName = userName;
    this.score = score;
}
```
#### 4. Prototype Methods
- Methods defined on the constructor function's prototype are shared across all instances.
- This ensures memory efficiency because the methods are not recreated for each instance.
##### Example:
```javascript
createUser.prototype.increment = function() {
    this.score++;
};
```
----


### Code Notes

#### Function Properties:
- Functions can have their own properties:
```javascript
function multiplyBY5(num) {
    return num * 5;
}
multiplyBY5.power = 2; // Adds a property.
console.log(multiplyBY5.power); // Output: 2
```

#### Function Prototype:
- The **`prototype`** property exists for functions but is generally used with constructor functions.
##### Example:
```javascript
console.log(multiplyBY5.prototype); // Output: {}
```

#### 3. Constructor Function Example:

- **`createUser`** is a constructor function used to create user objects with **`userName`** and score properties.
##### Example:
```javascript
const chai = new createUser("chai", 25);
console.log(chai); // { userName: 'chai', score: 25 }
```

#### 4. Adding Methods to the Prototype:
Shared methods, such as **`increment`** and **`printMe`**, are added to the prototype of **`createUser`**.
- These methods can be accessed by all instances:
```javascript
chai.increment(); // Increments the score for 'chai'.
chai.printMe();   // Logs the score: "Your Price is: 26".
```

### 5. Prototype Chain:
- When a method or property is called on an object, JavaScript first looks for it on the object itself. If not found, it looks up the prototype chain.
##### Example:
```javascript
chai.increment(); // Found on `createUser.prototype`.
```
--- 

### Key Concepts :

#### 1. Functions as Objects:
- Functions can store properties and methods.
- These properties are independent of the function's execution.

#### 2. Prototypes:
- Objects inherit from their constructor's `prototype`.
- Methods defined on the prototype are shared across all instances, saving memory.

#### 3. Constructor Functions:
 Use `this` to define instance-specific properties.
 Use `prototype` to define shared methods.

#### 4. Prototype Methods:
- Ensure methods like `increment` and `printMe` are available for all instances of `createUser`.

---
### Takeaways
- Functions in JavaScript are powerful objects that can have their own properties and prototypes.
- Constructor functions and prototypes are key to creating reusable and memory-efficient object structures.
- The `prototype` property allows sharing methods among all instances of an object, promoting efficiency and consistency.