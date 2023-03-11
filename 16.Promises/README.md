## Javascript Promises 
JavaScript Promise is a powerful feature that allows asynchronous operations in JavaScript to be handled in a more organized and efficient way. Promises are a way to handle the results of asynchronous operations, such as network requests, file I/O, or database queries.

A Promise represents a value that is not yet available, but will be available at some point in the future. It is a placeholder for a future value, or the result of an asynchronous operation. A Promise can be in one of three states:


* **Pending**: The initial state of a Promise. The Promise is neither fulfilled nor rejected.

* **Fulfilled**: The state of a Promise representing a successful operation.

* **Rejected**: The state of a Promise representing a failed operation.


A Promise is an object that represents the eventual result of an asynchronous operation. It is a proxy for a value not necessarily known when the promise is created. It allows you to associate handlers with an asynchronous action’s eventual success value or failure reason. This lets asynchronous methods return values like synchronous methods: instead of immediately returning the final value, the asynchronous method returns a promise to supply the value at some point in the future.

Here is a simple example of a Promise:

```javascript
let promise = new Promise(function(resolve, reject) {
  setTimeout(() => resolve("done!"), 1000)
});

// resolve runs the first function in .then
promise.then(
  result => alert(result), // shows "done!" after 1 second
  error => alert(error) // doesn't run
);
```


The Promise constructor takes one argument, a function, with two parameters, resolve and reject. These are functions that are pre-defined by JavaScript. The resolve function is called when the asynchronous operation is successful and the reject function is called when the asynchronous operation fails. The resolve and reject functions are called with a single argument, which is the value with which the promise is fulfilled or rejected. In the example above, the promise is fulfilled with the string "done!" after one second.


The then method takes two arguments, callback functions for the success and failure cases of the Promise. The first callback is called when the promise is resolved and the second callback is called when the promise is rejected. In the example above, the promise is resolved with the string "done!" after one second, so the first callback is called and the alert shows "done!".


Promises are used to handle asynchronous operations in JavaScript. They are easy to manage when dealing with multiple asynchronous operations where callbacks can create callback hell leading to unmanageable code. Promises provide a better way of handling asynchronous operations that are easier to read and maintain.


## Creating a Promise
A Promise is created using the new Promise constructor. It takes a single argument, a callback function, with two parameters, resolve and reject. The callback function is called immediately by the Promise implementation, passing resolve and reject functions (the executor). The resolve and reject functions, when called, resolve or reject the promise, respectively. The executor generally initiates some asynchronous work, and then, once that completes, either calls the resolve function to resolve the promise or else rejects it if an error occurred.


```javascript
let promise = new Promise(function(resolve, reject) {
  // executor (the producing code, "singer")
});
```

## Promise States
A Promise object can be in one of three states: pending, fulfilled, or rejected.

