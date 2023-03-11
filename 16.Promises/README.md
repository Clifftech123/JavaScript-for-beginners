## Javascript Promises 
JavaScript Promise is a powerful feature that allows asynchronous operations in JavaScript to be handled in a more organized and efficient way. Promises are a way to handle the results of asynchronous operations, such as network requests, file I/O, or database queries.

A Promise represents a value that is not yet available, but will be available at some point in the future. It is a placeholder for a future value, or the result of an asynchronous operation. A Promise can be in one of three states:


* **Pending**: The initial state of a Promise. The Promise is neither fulfilled nor rejected.

* **Fulfilled**: The state of a Promise representing a successful operation.

* **Rejected**: The state of a Promise representing a failed operation.

 Here is and example of a  how  to create promise :

```javascript
let promise = new Promise(function(resolve, reject) {
  // executor (the producing code, "singer")
});
```


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


The Promise constructor takes one argument, a function, with two parameters, resolve and reject. These are functions that are pre-defined by JavaScript. The resolve function is called when the asynchronous operation is successful and the reject function is called when the asynchronous operation fails. The resolve and reject functions are called with a single argument, which is the value with which the promise is fulfilled or rejected. In the example above, the promise is fulfilled with the string "done!" after one second




The then method takes two arguments, callback functions for the success and failure cases of the Promise. The first callback is called when the promise is resolved and the second callback is called when the promise is rejected. In the example above, the promise is resolved with the string "done!" after one second, so the first callback is called and the alert shows "done!".

Here is an example of a Promise that is rejected with an error:

```javascript

// the function is executed automatically when the promise is constructed

// after 1 second signal that the job is finished with an error

let promise = new Promise(function(resolve, reject) {
  setTimeout(() => reject(new Error("Whoops!")), 1000);
});


// reject runs the second function in .then
promise.then(
  result => alert(result), // doesn't run
  error => alert(error) // shows "Error: Whoops!" after 1 second
);
```

Promises are used to handle asynchronous operations in JavaScript. They are easy to manage when dealing with multiple asynchronous operations where callbacks can create callback hell leading to unmanageable code. Promises provide a better way of handling asynchronous operations that are easier to read and maintain.



```javascript
let promise = new Promise(function(resolve, reject) {
  // executor (the producing code, "singer")
});
```


To handle the result of a Promise, you can attach callbacks to the Promise using the then and catch methods. The then method is called when the Promise is fulfilled, and the catch method is called when the Promise is rejected.


Here is an example of using then and catch to handle the result of a Promise:

```javascript

promise
  .then(result => {
    // Handle the result of the successful operation
  })
  .catch(error => {
    // Handle the error from the failed operation
  });

```


Promises can also be chained together using the then method, which returns a new Promise. This allows for a sequence of asynchronous operations to be performed in order.

Here is an example of chaining Promises:

```javascript
promise1
  .then(result1 => {
    // Perform another asynchronous operation using result1
    return promise2;
  })
  .then(result2 => {
    // Perform another asynchronous operation using result2
    return promise3;
  })
  .then(result3 => {
    // Handle the final result of the asynchronous operations
  })
  .catch(error => {
    // Handle any errors from the asynchronous operations
  });

```

Let take look some core concepts of Promises:

## Pending Promises:

A pending Promise is a Promise that is not yet settled, meaning that it has neither fulfilled nor rejected. It represents an asynchronous operation that is still in progress and has not yet produced a result or an error.

When you create a Promise, it starts out in the pending state. The Promise remains in this state until it is either fulfilled or rejected. During this time, you can attach callbacks to the Promise using the then method. These callbacks will be executed when the Promise is settled, whether it is fulfilled or rejected.

Here is an example of a pending Promise:

```javascript
const promise = new Promise((resolve, reject) => {
  // Perform some asynchronous operation
  // If the operation is successful, call resolve with the result
  // If the operation fails, call reject with an error object
});

// The Promise is now in the pending state

```

In the above example, the Promise is created but it is still in the pending state because the asynchronous operation has not yet completed. Once the operation is complete, the Promise will either be fulfilled or rejected, depending on whether it was successful or not.

To handle the result of the Promise when it is settled, you can attach callbacks to it using the then method. Here is an example:

```javascript


promise
  .then(result => {
    // Handle the result of the successful operation
  })
  .catch(error => {
    // Handle the error from the failed operation
  });

```



## Fulfilled Promises:

A fulfilled Promise is a Promise that has been successfully completed. It represents an asynchronous operation that has completed successfully and produced a result.

When you create a Promise, it starts out in the pending state. The Promise remains in this state until it is either fulfilled or rejected. If the asynchronous operation is successful, the Promise is fulfilled with the result of the operation. If the asynchronous operation fails, the Promise is rejected with an error object.


Here is an example of a fulfilled Promise:

```javascript

const promise = new Promise((resolve, reject) => {
  // Perform some asynchronous operation
  // If the operation is successful, call resolve with the result
  // If the operation fails, call reject with an error object
  resolve('Success!');
});



// The Promise is now in the pending state

// The Promise is now in the fulfilled state

```

In the above example, the Promise is created but it is still in the pending state because the asynchronous operation has not yet completed. Once the operation is complete, the Promise is fulfilled with the result of the operation.


To handle the result of the Promise when it is settled, you can attach callbacks to it using the then method. Here is an example:

```javascript

promise
  .then(result => {
    // Handle the result of the successful operation
  })
  .catch(error => {
    // Handle the error from the failed operation
  });

```


## Rejected Promises:

A rejected Promise is a Promise that has been rejected. It represents an asynchronous operation that has failed and produced an error.

When you create a Promise, it starts out in the pending state. The Promise remains in this state until it is either fulfilled or rejected. If the asynchronous operation is successful, the Promise is fulfilled with the result of the operation. If the asynchronous operation fails, the Promise is rejected with an error object.


Here is an example of a rejected Promise:

```javascript

const promise = new Promise((resolve, reject) => {
  // Perform some asynchronous operation
  // If the operation is successful, call resolve with the result
  // If the operation fails, call reject with an error object
  reject(new Error('Error!'));
});



// The Promise is now in the pending state

// The Promise is now in the rejected state

```


In the above example, the Promise is created but it is still in the pending state because the asynchronous operation has not yet completed. Once the operation is complete, the Promise is rejected with the error object.


To handle the result of the Promise when it is settled, you can attach callbacks to it using the then method. Here is an example:

```javascript

promise
  .then(result => {
    // Handle the result of the successful operation
  })
  .catch(error => {
    // Handle the error from the failed operation
  });

```

## Promise Chaining:

Promises can be chained together using the then method, which returns a new Promise. This allows for a sequence of asynchronous operations to be performed in order.

Here is an example of chaining Promises:

```javascript

promise1
  .then(result1 => {
    // Perform another asynchronous operation using result1
    return promise2;
  })
  .then(result2 => {
    // Perform another asynchronous operation using result2
    return promise3;
  })
  .then(result3 => {
    // Handle the final result of the asynchronous operations
  })
  .catch(error => {
    // Handle any errors from the asynchronous operations
  });

```


In the above example, the first then method is called when the promise1 is fulfilled. The result of the promise1 is passed to the first then method as the result1 parameter. The first then method performs another asynchronous operation using the result1 and returns a new Promise, promise2. The second then method is called when the promise2 is fulfilled. The result of the promise2 is passed to the second then method as the result2 parameter. The second then method performs another asynchronous operation using the result2 and returns a new Promise, promise3. The third then method is called when the promise3 is fulfilled. The result of the promise3 is passed to the third then method as the result3 parameter. The third then method handles the final result of the asynchronous operations. If any of the asynchronous operations fail, the catch method is called with the error object.


## Promise.all:

The Promise.all method takes an array of Promises as an argument and returns a single Promise. The single Promise returned by the Promise.all method is fulfilled when all of the Promises in the argument array are fulfilled. The single Promise returned by the Promise.all method is rejected when any of the Promises in the argument array are rejected.


Here is an example of using the Promise.all method:

```javascript

const promise1 = new Promise((resolve, reject) => {
  setTimeout(resolve, 1000, 'one');
});

const promise2 = new Promise((resolve, reject) => {
  setTimeout(resolve, 2000, 'two');
});

const promise3 = new Promise((resolve, reject) => {
  setTimeout(resolve, 3000, 'three');
});


Promise.all([promise1, promise2, promise3])
  .then(values => {
    // Handle the result of the asynchronous operations
  })
  .catch(error => {
    // Handle any errors from the asynchronous operations
  });

```


In the above example, three Promises are created, promise1, promise2, and promise3. The Promise.all method is called with an array containing the three Promises as an argument. The Promise returned by the Promise.all method is fulfilled when all of the Promises in the argument array are fulfilled. The Promise returned by the Promise.all method is rejected when any of the Promises in the argument array are rejected. The then method is called when the Promise returned by the Promise.all method is fulfilled. The values parameter contains an array of the results of the asynchronous operations. The catch method is called when the Promise returned by the Promise.all method is rejected. The error parameter contains the error object.



In conclusion, Promises are a great way to handle asynchronous operations in JavaScript. They are a great alternative to using callbacks and they make your code easier to read and maintain. I hope you found this article helpful. If you have any questions or comments, please leave them below. Thanks for reading!


You can find more Resources  below:

## Resources:

* [MDN - Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)

* [MDN - Promise.prototype.then](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/then)

* [MDN - Promise.prototype.catch](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/catch)

* [MDN - Promise.all](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/all)

* [MDN - Promise.resolve](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/resolve)

* [MDN - Promise.reject](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/reject)


## Other Articles:

* [JavaScript Promises for Dummies](https://medium.com/@stasonmars/%D0%BF%D1%80%D0%BE%D0%BC%D0%B8%D1%81%D1%8B-%D0%B2-javascript-%D0%B4%D0%BB%D1%8F-%D0%BD%D0%B0%D1%87%D0%B8%D0%BD%D0%B0%D1%8E%D1%89%D0%B8%D1%85-1a8b0d9a8b0d)

* [JavaScript Promises for Dummies - Part 2](https://medium.com/@stasonmars/javascript-promises-for-dummies-part-2-3f1b4b0b0d5a)

* [JavaScript Promises for Dummies - Part 3](https://medium.com/@stasonmars/javascript-promises-for-dummies-part-3-4f2a5e6a3f1b)

* [JavaScript Promises for Dummies - Part 4](https://medium.com/@stasonmars/javascript-promises-for-dummies-part-4-5f1b4b0b0d5a)

* [JavaScript Promises for Dummies - Part 5](https://medium.com/@stasonmars/javascript-promises-for-dummies-part-5-6f1b4b0b0d5a)

* [JavaScript Promises for Dummies - Part 6](https://medium.com/@stasonmars/javascript-promises-for-dummies-part-6-7f1b4b0b0d5a)

* [JavaScript Promises for Dummies - Part 7](https://medium.com/@stasonmars/javascript-promises-for-dummies-part-7-8f1b4b0b0d5a)

* [JavaScript Promises for Dummies - Part 8](https://medium.com/@stasonmars/javascript-promises-for-dummies-part-8-9f1b4b0b0d5a)











