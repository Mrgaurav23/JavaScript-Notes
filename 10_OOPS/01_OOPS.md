# OOPS ->

## Definitions

### 1. Object Literals:
- An Object Literal is the simplest and most direct way to create an object in JavaScript.
- It allows you to define an object by enclosing key-value pairs inside curly braces `{}`.
##### Example:
```javascript
const user = {
    username: "Ravindra",
    loginCount: 8,
    signedIn: true,
    getUserDetails: function() {
        console.log(`Username: ${this.username}`);
        console.log(this);
    }
};
```
### 2. Constructor Functions:
- A **Constructor Function** is a special type of function used to create and initialize objects with similar properties and methods.
- Constructor functions use the `this` keyword to define properties and methods for the object being created.
##### Example:
```javascript
function User(userName, loginCount, isLoggedIn) {
    this.userName = userName;
    this.loginCount = loginCount;
    this.isLoggedIn = isLoggedIn;

    this.greeting = function(){
        console.log(`Welcome: ${this.userName}`);
    }
    return this;
}
const userOne = new User("Ravindra", 5, true);
```
### 3. `this` Keyword:
- Refers to the current context or the object that is calling the function.
- Its behavior changes depending on where it is used:
    - In object methods: Refers to the object.
    - In global functions or constructors: Refers to the global object (or the instance in case of constructors).

### 4. Object's constructor Property:
The constructor property returns the function that created the object's prototype.
##### Example:
```javascript
//Constructor
const userOne = new User("Ravindra", 5, true);
console.log(userOne.constructor); // Outputs: User
```
---

### Takeaways
- Object Literals are simple and best for single objects.
- Constructor Functions provide a reusable structure for creating multiple objects.
- The **`this`** keyword is crucial for understanding object methods and constructors.
- The **`constructor`** property helps identify the function used to create an object.

---