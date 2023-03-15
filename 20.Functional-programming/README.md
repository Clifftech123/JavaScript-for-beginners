## Function Pogroming in Javascript

Functional programming is a programming paradigm that emphasizes the use of functions to write programs. In functional programming, functions are treated as first-class citizens, meaning that they can be passed as arguments to other functions, returned as values from functions, and stored in variables or data structures. JavaScript is a multi-paradigm language that supports functional programming, among other programming paradigms.

Functional programming in JavaScript involves writing code that focuses on creating pure functions and avoiding side effects. A pure function is a function that always returns the same output for the same input and does not modify any state outside of its scope. This makes it easier to reason about the behavior of the code and helps avoid bugs caused by unexpected changes to state.

- Higher-order functions : A higher-order function is a function that takes a function as an argument or returns a function as a return value. Higher-order functions are often used to abstract or isolate actions, effects, or async flow control using callback functions, promises, or monads.

here is an example of a higher-order function that takes a function as an argument:

```js
// Higher-order function

function higherOrderFunction(callback) {
  return callback();
}
function callbackFunction() {
  console.log("I am a callback function!");
}
higherOrderFunction(callbackFunction); // Output: I am a callback function!
```

- Pure functions : A pure function is a function that always returns the same output for the same input and does not modify any state outside of its scope. This makes it easier to reason about the behavior of the code and helps avoid bugs caused by unexpected changes to state.

```js
// Pure function

function sum(a, b) {
  return a + b;
}
sum(1, 2); // Output: 3
```

- Immutability : Immutability is a concept that is often used in functional programming. In JavaScript, this means that data structures cannot be modified after they are created. Instead, new data structures are created that contain the modified values. This makes it easier to reason about the state of the program and helps avoid bugs caused by unexpected changes to state.
  Here is an example of an immutable array:

```js
// Immutable array

const numbers = [1, 2, 3];
const newNumbers = [...numbers, 4]; // Output: [1, 2, 3, 4]
```

- Recursion : Recursion is a technique for iterating over an operation by having a function call itself repeatedly until it arrives at a result. Recursion is often used to traverse data structures such as trees and graphs. Here is an example of a recursive function that traverses a tree:

```js
// Recursive function

function traverseTree(node) {
  if (node === null) {
    return;
  }
  traverseTree(node.left);
  traverseTree(node.right);
}
```

- Currying : Currying is a technique for transforming a function that takes multiple arguments into a sequence of functions that each take a single argument. Currying is often used to create higher-order functions. Here is an example of a curried function:

```js
// Curried function

function curriedAdd(a) {
  return function (b) {
    return a + b;
  };
}
const addOne = curriedAdd(1);
const addTen = curriedAdd(10);
addOne(2); // Output: 3 addTen(2); // Output: 12
```

- Partial application : Partial application is a technique for creating a new function by fixing some of the arguments of an existing function. This can be useful when you want to create a new function with some of the arguments already set. Here is an example of a partially applied function:

```js
// Partially applied function

function add(a, b) {
  return a + b;
}
const addOne = add.bind(null, 1);
addOne(2); // Output: 3
```

- Memoization : Memoization is a technique for caching the results of a function based on its arguments. This can be useful when you want to avoid doing expensive calculations multiple times. Here is an example of a memoized function:

```js
// Memoized function

function memoizedAddTo25() {
  let cache = {};
  return function (n) {
    if (n in cache) {
      console.log("Fetching from cache");
      return cache[n];
    } else {
      console.log("Calculating result");
      let result = n + 25;
      cache[n] = result;
      return result;
    }
  };
}
const memoized = memoizedAddTo25();
memoized(10); // Output: Calculating result // Output: 35 memoized(10); // Output: Fetching from cache // Output: 35
```

- Composing functions : Composing functions is a technique for combining two or more functions to produce a new function. This can be useful when you want to abstract a complex operation into a series of simpler steps. Here is an example of a composed function:

```js
// Composed function

function compose(f, g) {
  return function (x) {
    return f(g(x));
  };
}
function addOne(x) {
  return x + 1;
}
function addFive(x) {
  return x + 5;
}
const addSix = compose(addOne, addFive);
addSix(0); // Output: 6
```

- Point-free style : Point-free style is a technique for writing functions without explicitly mentioning the arguments. This can be useful when you want to abstract a complex operation into a series of simpler steps. Here is an example of a point-free function:

```js
// Point-free function

function compose(f, g) {
  return function (x) {
    return f(g(x));
  };
}
function addOne(x) {
  return x + 1;
}
function addFive(x) {
  return x + 5;
}
const addSix = compose(addOne, addFive);
addSix(0); // Output: 6
```

- Function composition : Function composition is a technique for combining two or more functions to produce a new function. This can be useful when you want to abstract a complex operation into a series of simpler steps. Here is an example of a composed function:

```js
// Composed function

function compose(f, g) {
  return function (x) {
    return f(g(x));
  };
}
function addOne(x) {
  return x + 1;
}
function addFive(x) {
  return x + 5;
}
const addSix = compose(addOne, addFive);
addSix(0); // Output: 6
```
