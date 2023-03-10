## Error Handling in javascript 

- **What is Error Handling in javascript?**

Error handling in JavaScript is the process of anticipating, detecting, and resolving errors that may occur during the execution of a JavaScript program. There are several ways to handle errors in JavaScript: using try...catch, throw, finally, Error object, error handling in async functions, error handling in promises, error handling in callbacks, error handling in event listeners, and error handling in event handlers.

- **Using try...catch**
try-catch: The try-catch statement is used to handle exceptions that may occur in a block of code. The code that may throw an exception is enclosed in a try block, and the exception is caught and handled in the catch block.

```js 

// Example 1
// try-catch example
try {
  // code that may throw an exception
} catch (err) {
  // code that handles the exception
}

// Example 2 
 // try-catch example
 const asyncFunction = async () => {
  try {
    await Promise.reject('Error');
  } catch (error) {
    console.log(error);
  }
```

- **Using throw**

 The throw statement is used to manually throw an exception. This is useful when you want to create your own custom error message.

```js
// Example 1
// throw example
throw new Error('Something went wrong');

// Example 2
// throw example
function myFunction() {
  try {
    throw 'myException'; // generates an exception
  }
  catch (e) {
    // statements to handle any exceptions
    logMyErrors(e); // pass exception object to error handler
  }
}
```

- **Using finally**

 The finally block is used to execute code after the try and catch blocks, regardless of whether an exception was thrown or not.

```js
// Example 1
// finally example
try {
  // code that may throw an exception
} catch (err) {
  // code that handles the exception
} finally {
  // code that will always execute
}

// Example 2
// finally example
function myFunction() {
  try {
    throw 'myException'; // generates an exception
  }
  catch (e) {
    // statements to handle any exceptions
    logMyErrors(e); // pass exception object to error handler
  }
  finally {
    // statements to be executed
    // regardless of exception thrown or not
  }
}
```

- **Error object**

JavaScript provides several built-in error objects, such as Error, RangeError, TypeError, etc., which can be used to create custom error messages.

```js

// Example 1
// Error object example
const error = new Error('Something went wrong');

// Example 2
// RangeError object example
const error = new RangeError('Something went wrong');

// Example 3
// TypeError object example
const error = new TypeError('Something went wrong');
```

- **Error handling in async functions**

The try-catch statement can be used to handle errors in async functions. The await keyword is used to wait for a promise to be resolved or rejected.

```js
// Example 1
// Error handling in async functions
const asyncFunction = async () => {
  try {
    await Promise.reject('Error');
  } catch (error) {
    console.log(error);
  }
}

```


- **Error handling in promises**

The catch() method is used to handle errors in promises. The catch() method returns a Promise and deals with rejected cases only. It behaves the same as the try-catch block for errors.

```js

// Example 1
// Error handling in promises
const promise = new Promise((resolve, reject) => {
  reject('Error');
});

promise.catch((error) => {
  console.log(error);
});

// Example 2

// Error handling in promises
const promise = new Promise((resolve, reject) => {
  reject('Error');
});

promise
  .then((data) => {
    console.log(data);
  })
  .catch((error) => {
    console.log(error);
  });
```


- **Error handling in callbacks**

The callback function is the last argument of the function. The callback function is called after the function is executed. The callback function is used to handle errors in callbacks.

```js
// Example 1

// Error handling in callbacks
const callbackFunction = (error, data) => {
  if (error) {
    console.log(error);
  } else {
    console.log(data);
  }
};

const asyncFunction = (callback) => {
  callback('Error', null);
};

asyncFunction(callbackFunction);

// Example 2

// Error handling in callbacks
const callbackFunction = (error, data) => {
  if (error) {
    console.log(error);
  } else {
    console.log(data);
  }
};

const asyncFunction = (callback) => {
  callback(null, 'Data');
};


```


- **Error handling in event listeners**

The addEventListener() method is used to handle errors in event listeners. The addEventListener() method attaches an event handler to the specified element.

```js

// Example 1
// Error handling in event listeners
const button = document.querySelector('button');

button.addEventListener('click', () => {
  throw new Error('Something went wrong');
});

// Example 2

// Error handling in event listeners
const button = document.querySelector('button');

button.addEventListener('click', () => {
  console.log('Button clicked');
});
```

- **Error handling in event handlers**

The event handler is a function that is called when an event occurs. The event handler is used to handle errors in event handlers.

```js

// Example 1
// Error handling in event handlers
const button = document.querySelector('button');

button.onclick = () => {
  throw new Error('Something went wrong');
};


```



- **What is the difference between throw and reject?**

The throw statement is used to manually throw an exception. The reject() method is used to reject a promise. The throw statement is used to create custom error messages. The reject() method is used to create custom error messages for promises.

```js

// Example 1
// throw example
throw new Error('Something went wrong');

// Example 2
// reject example
const promise = new Promise((resolve, reject) => {
  reject('Error');
});

promise.catch((error) => {
  console.log(error);
});
```


Error is important in javascript and you must know how to handle it. I hope this article will help you to understand error handling in javascript. If you have any questions, please leave a comment below. Thank you for reading this article. Happy coding!


You can find the source code of this article here:

## Resources

- [Error handling in JavaScript](https://www.freecodecamp.org/news/error-handling-in-javascript/)

- [Error handling in JavaScript](https://www.javascripttutorial.net/javascript-error-handling/)

- [Error handling in JavaScript](https://www.tutorialsteacher.com/javascript/error-handling-in-javascript)
