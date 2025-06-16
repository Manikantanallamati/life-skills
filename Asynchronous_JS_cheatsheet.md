## **Asynchronous JavaScript Concepts - Cheat Sheet**

---
### 1. How JavaScript Executes the Code

JavaScript uses a **single-threaded**, **non-blocking**, **event-driven** execution model. It has a **call stack** where function calls are executed line-by-line. For asynchronous operations, it relies on **Web APIs**, **Callback Queues**, and the **Event Loop** to manage and execute deferred tasks efficiently.

### 2. Synchronous vs Asynchronous

**Synchronous** code runs sequentially; one operation completes before the next begins. **Asynchronous** code allows the execution to continue while waiting for slower operations like API calls or timers, preventing blocking.

| Feature   | Synchronous  | Asynchronous           |
| --------- | ------------ | ---------------------- |
| Execution | Sequential   | Non-blocking           |
| Thread    | Single       | Single + Web APIs      |
| Use Case  | Simple logic | I/O operations, Timers |

### 3. Ways to Make Code Asynchronous

* **Callbacks**
* **Promises**
* **async/await**
* **Web APIs like setTimeout, fetch**

### 4. Web Browser APIs

Web Browser APIs are features provided by the browser (not JavaScript itself). Examples:

* **setTimeout / setInterval**
* **fetch API**
* **DOM manipulation**
* **Geolocation, WebSockets, Storage APIs**
  These APIs handle asynchronous operations outside the call stack.

### 5. Event Loop

The Event Loop is a mechanism that watches the **Call Stack** and **Callback Queue**. When the stack is empty, the Event Loop pushes queued callbacks into the stack to be executed.

---

## Promises

### 6. What is Callback Hell?

Callback hell refers to deeply nested callbacks, making code hard to read and maintain.

```js
step1(() => {
  step2(() => {
    step3(() => {
      // so on
    });
  });
});
```

### 7. What is Inversion of Control?

In callbacks, we give control of the execution to external code, making debugging and maintenance harder. This is called inversion of control.

### 8. What is a Promise?

A **Promise** is an object representing the eventual completion or failure of an asynchronous operation.

### 9. How to Create a New Promise

```js
const promise = new Promise((resolve, reject) => {
  if (success) resolve(data);
  else reject(error);
});
```

### 10. States of a Promise

* **Pending** – initial state
* **Fulfilled** – completed successfully
* **Rejected** – failed

### 11. How to Consume an Existing Promise

```js
promise.then(result => console.log(result)).catch(error => console.error(error));
```

### 12. Chaining Promises Using .then

```js
fetch(url)
  .then(res => res.json())
  .then(data => process(data))
  .catch(err => console.error(err));
```

### 13. Handling Errors Using .catch

`.catch()` handles any error that occurs in the chain.

### 14. finally Block in a Promise Chain

Executes after the promise settles (either fulfilled or rejected).

```js
promise.finally(() => console.log("Cleanup"));
```

### 15. Error Inside .then with .catch

The error is caught by the `.catch()` in the chain.

### 16. Error Inside .then with No .catch

The error is unhandled and results in an uncaught promise rejection.

### 17. Why .catch Should Be at the End

Placing `.catch()` at the end ensures all errors in the promise chain are handled.

### 18. Consuming Multiple Promises by Chaining

```js
fetch(url1)
  .then(res => fetch(url2))
  .then(res => fetch(url3))
```

### 19. Consuming Multiple Promises with Promise.all

```js
Promise.all([p1, p2, p3]).then(values => console.log(values));
```

Fails fast – rejects if any one fails.

### 20. Error Handling in Promises

Use `.catch()` or `try/catch` inside async/await functions.

```js
async function getData() {
  try {
    let result = await fetch(url);
  } catch (error) {
    console.error(error);
  }
}
```

### 21. Importance of Error Handling in Promises

Failing to handle errors causes unhandled promise rejections and unstable applications.

### 22. How to Promisify Callback-based APIs

```js
function delay(ms) {
  return new Promise(resolve => setTimeout(resolve, ms));
}
delay(1000).then(() => console.log("Waited 1 second"));
```

---

## Built-in Promise Methods

### 23. Promise.resolve

Returns a resolved promise.

```js
Promise.resolve("OK").then(console.log);
```

### 24. Promise.reject

Returns a rejected promise.

```js
Promise.reject("Error").catch(console.error);
```

### 25. Promise.all

Waits for all promises; rejects if any fail.

```js
Promise.all([p1, p2]);
```

### 26. Promise.allSettled

Waits for all promises to finish, regardless of result.

```js
Promise.allSettled([p1, p2]).then(console.log);
```

### 27. Promise.any

Resolves with first successful promise.

```js
Promise.any([p1, p2]).then(console.log);
```

### 28. Promise.race

Resolves/rejects as soon as any promise settles.

```js
Promise.race([p1, p2]).then(console.log);
```


