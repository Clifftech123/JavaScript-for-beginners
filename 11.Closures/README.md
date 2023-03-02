 ## Closures  in javascript

- **What is a closure in javascript?**

Closures are a fundamental concept in JavaScript that allow for powerful and flexible programming techniques. Essentially, a closure is created whenever a function is defined inside another function, and the inner function retains access to the variables and scope of the outer function, even after the outer function has completed execution. A closure is a function that has access to the parent scope, even after the parent function has closed.

Here is a simple example:
    
```javascript
    // closure Example
    function outer() {
  var x = 10;
  
  function inner() {
    console.log(x);
  }
  
  return inner;
}

var innerFn = outer();
innerFn(); // output: 10
```

In this example, the outer function creates a variable x and a nested function inner. outer then returns inner, and the variable innerFn is assigned the result of calling outer. Finally, innerFn is called, which prints out the value of x (which is 10) to the console.

What's happening here is that the inner function forms a closure over the variables and scope of outer. Even though outer has completed execution and its variables should no longer be accessible, the closure ensures that inner retains access to those variables.

One of the key benefits of closures is that they allow for data privacy and encapsulation. In the example above, the variable x is not accessible from outside the outer function - it can only be accessed by calling the inner function, which has access to the closure.


Closures are also commonly used in functional programming techniques such as currying and partial application. Here's an example of how closures can be used to create a curried function:
```javascript
    // closure Example
   function add(a) {
  return function(b) {
    return a + b;
  }
}

var add5 = add(5);
console.log(add5(3)); // output: 8

```

In this example, the add function returns a new function that takes a single argument b and returns the sum of a and b. The value of a is retained in the closure, allowing the returned function to be "curried" with a specific value of a. The add5 variable is assigned the result of calling add(5), which creates a new function that adds 5 to its argument. When add5 is called with an argument of 3, it returns 8.

Overall, closures are a powerful and important concept in JavaScript that enable a wide range of programming techniques. By understanding how closures work and how to use them effectively, you can write more flexible, expressive, and maintainable code.



### Resources
You can find more information about closures in the following resources:

- [MDN: Closures](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures)

