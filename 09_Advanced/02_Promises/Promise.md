# Promises & async await

## Definitions
### 1. Promises
A Promise in JavaScript is an object that represents the eventual completion (or failure) of an asynchronous operation and its resulting value. It provides a cleaner way to handle asynchronous tasks compared to traditional callback functions.

#### States of a Promise:
- **Pending**: Initial state, neither fulfilled nor rejected.
- **Fulfilled**: The operation completed successfully.
- **Rejected**: The operation failed.

#### Key Methods:

- **`.then(onFulfilled, onRejected)`** – Executes on fulfillment or rejection.
- **`.catch(onRejected)`** – Handles errors or rejections.
- **`.finally(callback)`** – Executes after the promise is settled (resolved or rejected).

---

### 2. Async/Await
**Async/Await** is syntactic sugar over Promises that makes asynchronous code look and behave more like synchronous code. It improves readability and is easier to debug.
- **`async`**:
   - Declares a function as asynchronous.
   - The function automatically returns a Promise.

- **`await`**:
   - Pauses the execution of an async function until the Promise is resolved or rejected.

---
### 3. Fetch API
The Fetch API is used to make **HTTP requests**. It returns a Promise that resolves to the response of the request.
##### Example:
``` javascript
fetch("https://example.com/api")
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.log(error));
```

---

##### Task 1 Completed.
```javaScript
const promiseOne = new Promise(function(resolve,reject){
    //Do an async task
    //DB calls, cryptography, network
    setTimeout(function(){
        console.log("Async task 1 completed");
        resolve();
    },1000)
})
promiseOne.then(function(){
    console.log("Completed task");
})
```

##### Task 2 Completed.
```javascript
new Promise(function(resolve,reject){
    setTimeout(function(){
        console.log("Async task 2 completed");
        resolve();
    },1000)
}).then(function(){
    console.log("Completed Task 2");
})
```


##### Task 3 Completed.
```javascript
const promiseThree = new Promise(function(resolve,reject){
    setTimeout(function(){
        console.log("Async 3 completed");
        resolve({userName:"Ravindra",email:"Ravindraexample@gmail.com",age:22,});
    },1000)
})
promiseThree.then(function(user){
    console.log(user);
})
```


##### Task 4 Completed
```javascript
const promiseFour = new Promise(function(resolve,reject){
    setTimeout(() => {
        let error = true;
        if(!error){
            resolve({userName:"Ravindra",email:"Ravindraexample@gmail.com",age:22,})
        }
        else{
            reject("Something Went Wrong");
        }
    }, 1000);
})
promiseFour.then(function(user){
    console.log(user);
}).catch(function(error){
    console.log(error);
})
```

##### Task 5 Completed.
```javascript
const promiseFive = new Promise( (resolve,reject) => {
    setTimeout( () => {
        let error = false;
        if(!error){
            resolve({userName: "Gaurav Singh",age: 22,isLoggedIn: "true"});
        }
        else{
            reject("Error : SomeThing Went Wrong");
        }
    },1000)
})

promiseFive.then((user) =>{
    return user.userName;
})
.then( (userName)=>{
    console.log(userName);
})
.catch( (error) =>{
    console.log(error);
})
.finally(() =>{
    console.log("The promise is either resolved or rejected");
})
```

##### Task 6
```javascript
const promiseSix = new Promise(function(resolve,reject) {
    setTimeout( () => {
        let error = true;
        if(!error){
            resolve({userName:"javaScript",email:"jsexample@gmail.com",age:22,});
        }
        else{
            reject("Error : SomeThing Went Wrong");
        }
    },1000)
})
```

---

### Key Concepts :

##### 1. Promise Creation:

```javascript
const promise = new Promise((resolve, reject) => {
    // Perform asynchronous task
    if (successCondition) {
        resolve(data);
    } else {
        reject(error);
    }
});
```

##### 2. Promise Methods:

- **Chaining**:
```javascript
promise
  .then(result => console.log(result))
  .catch(error => console.log(error))
  .finally(() => console.log("Done"));
```
- **Error Handling**: Use `.catch` to handle rejections in promises.

##### 3. Async/Await:
- Simplifies promise consumption:
``` javascript
async function fetchData() {
    try {
        const response = await fetch("https://api.example.com");
        const data = await response.json();
        console.log(data);
    } catch (error) {
        console.log("Error:", error);
    }
}
```
##### 4. Fetch API:

- **Usage**:
```javascript
fetch("https://api.example.com")
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.log(error));
```
---

#### Key Takeaways
- Promises simplify asynchronous programming, making code cleaner and easier to follow.
- Async/await is syntactic sugar that makes promises easier to work with, offering better readability.
- The Fetch API is a modern way to perform HTTP requests and works seamlessly with Promises and async/await.
- Proper error handling is critical in asynchronous operations to ensure program stability.
