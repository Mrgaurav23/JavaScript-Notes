# API_Request ->

## Defination :
This code demonstrates how to use the **`XMLHttpRequest`** object in JavaScript to interact with an API. The API in this case (**`https://randomuser.me/api/`**) provides random user data. The script sends a GET request to the API, processes the response, and logs the received data.

The **`XMLHttpRequest`** is a built-in browser object that allows making HTTP requests to servers, fetching data, and handling server responses, typically in formats like JSON.

### Code Explanation :
### 1. `XMLHttpRequest`:
- `XMLHttpRequest` is used to interact with servers via HTTP.
- Common methods:
- `open(method, url)`: Initializes the request with a method (`GET`, `POST`, etc.) and a URL.
`send()`: Sends the request to the server.
##### Example in the code:
```javascript
const xhr = new XMLHttpRequest();
xhr.open('GET', requestURL);
xhr.send();
```

### 2. `readystatechange` Event:
The `onreadystatechange` property defines a function to be called whenever the `readyState` of the `XMLHttpRequest` changes.
- **Common readyState values**:
- 0: `UNSENT` - Request is not initialized.
- 1: `OPENED` - Request has been set up.
- 2: `HEADERS_RECEIVED` - Headers have been received.
- 3: `LOADING` - The response body is being received.
- 4: `DONE` - The operation is complete.
##### In the code:
``` javascript
xhr.onreadystatechange = function() {
    console.log(xhr.readyState); // Logs the current state.
    if (xhr.readyState === 4) {
        const data = JSON.parse(this.responseText);
        console.log(data);
    }
};
```

### 3. JSON.parse():
Converts a JSON string into a JavaScript object.
##### Example in the code:
```javascript
const data = JSON.parse(this.responseText);
console.log(data);
```

### 4. API Response:
The code fetches data from `https://randomuser.me/api/`, which returns user data in JSON format.
##### Example response structure:
```javascript
{
  "results": [...],
  "info": {
    "seed": "value",
    "results": 1,
    ...
  }
}
```

### 5. Accessing JSON Properties:

Accessing nested properties is done using dot notation.
##### Examples in the code:
```javascript
console.log(data.info); // Logs the "info" object.
console.log(data.info.seed); // Logs the "seed" value.
```

### 6. Usage of V8 Engine:

The V8 engine is Google’s open-source JavaScript engine that compiles and executes JavaScript. It powers browsers like Chrome and runtimes like Node.js.

---

### Key Notes
- **Advantages of `XMLHttpRequest`**:
- Widely supported for making HTTP requests.
- Can handle both synchronous and asynchronous requests.
- **Limitations**:
- Verbose syntax compared to modern alternatives like `fetch`.
Requires handling `readyState` and response parsing manually.
---

#### Comparison to Modern Techniques
- **Fetch API**:
- Provides a cleaner syntax for making HTTP requests.
- Example:
```javascript
fetch(requestURL)
  .then(response => response.json())
  .then(data => console.log(data));
```
---

### Learning Takeaways
1. Understand how to use `XMLHttpRequest` for server communication.
2. Learn about JSON parsing and accessing nested properties in an object.
3. Appreciate the evolution of JavaScript with modern tools like the Fetch API and V8 Engine.