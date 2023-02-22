## JavaScript  Functions ## 

Functions are one of the fundamental concepts in programming. They let us write concise, modular, reusable, and maintainable code. They also help us obey the DRY principle when writing code. In this section , you will learn what functions are in JavaScript, how to write your own custom functions, and how to implement them.

**What is a Function in JavaScript?**
JavaScript functions are blocks of code that can be used repeatedly to perform a specific task. They're a crucial aspect of JavaScript programming and are widely utilized in both front-end and back-end web development. There are various ways to define functions in JavaScript, including:
* **Function Declaration**
* **Function Parameters**
* **Function Return Value**
* **Function Expression**
* **Arrow Function**
*  **Higher-Order Function**

Each of these methods has its unique features and benefits, allowing developers to write clean and efficient code. By using functions, developers can avoid repeating code and make their programs more modular and reusable.

let's take it one by one in details.

**Function Declaration**

A function can be declared in JavaScript using the function keyword followed by the function name and a set of parentheses. The parentheses can contain a list of parameters, which are variables that are passed to the function. The function body is enclosed in curly braces. Here's an example:

```javascript

// function declaration example
function myFunction() {
    // code to be executed
}

// example 2 
function myFunction(a, b) {
    // code to be executed
}

 // example 3
 function sayHello() {
  console.log('Hello!');
}
```
An important thing to note is that function declarations are hoisted. This means that you can call a function before it is declared in your code. For example:

```javascript
sayHello(); // Hello!

function sayHello() {
  console.log('Hello!');
}
```

**Function Parameters**

A function can accept input values or parameters by specifying them in the parentheses after the function name. 
For example:
  
  ```javascript
  // function with parameters
  function myFunction(value) {
    console.log(value);

function sayHello() {
  console.log('Hello!');
}


  // function with multiple parameters
  function myFunction(value1, value2) {
    console.log(value1, value2);

    function  myFunction( firstName, LastName) {
      console.log(`Hello your Name is ${firsName} + ${lastName }`); // first name  + last name 
    }
   //  
    }
  }
  ```
function parameters are optional. If a function does not have any parameters, you can still call it by using empty parentheses. For example:

```javascript
function sayHello() {
  console.log('Hello!');
}

sayHello(); // Hello!
```


**Function Return Value**
A function can return a value by using the return keyword. 
For example:
  
  ```javascript
  // function with return value
  function myFunction(value) {
    return value;
  }

 function myFunction(name) {
    return name;
  }


  // function with multiple return values
  function myFunction(value1, value2) {
    return [value1, value2];
  }


  function sum(a, b) {
  return a + b;
}
  ```

**Function Expression**
A function expression is a function that is assigned to a variable.
For example:
  
  ```javascript
  // function expression example
  const myFunction = function() {
    // code to be executed
  };

  const sayHello = function() {
  console.log('Hello!');
};

  // function expression with parameters
  const myFunction = function(value) {
    // code to be executed
  };

  const sayHello = function(name) {
  console.log(`Hello ${name}!`);
};

  // function expression with return value
  const myFunction = function(value) {
    return value;
  };

  const sum = function(a, b) {
  return a + b;
};
  ```

**Arrow Function**

An arrow function is a concise way to write a function expression. It is a shorter syntax for a function expression and does not have its own this, arguments, super, or new.target. Arrow functions are always anonymous. They cannot be used as constructors and do not have a prototype property.
For example:
  
  ```javascript
  // arrow function example
  const myFunction = () => {
    // code to be executed
  };

  const sayHello = () => {
  console.log('Hello!'); // Hello!
};

  // arrow function with parameters
  const myFunction = (value) => {
    // code to be executed
  };

  const sayHello = (name) => {
  console.log(`Hello ${name}!`); // Hello  name!
};

  // arrow function with return value
  const myFunction = (value) => {
    return value;
    console.log(value); // 5
  };
  // call the function
 myFunction(5); //  passing  5  to the function  and we can see the value 5  in the console


  const sum = (a, b) => {
  return a + b;

  console.log(a + b); // 8
};

// call the function
sum(5, 3); //  passing the value of the 5 and 3 and add it and   we can see the value of 8  in the console

  ```

**Higher-Order Function**

A higher-order function is a function that takes a function as an argument or returns a function. Higher-order functions are also known as functional programming. They are used to create abstractions and reduce code duplication. They are also used to create higher-level functions that can be used to solve complex problems.

For example:
  
  ```javascript
  // higher-order function example
  function myFunction(callback) {
    callback();
  }

function applyOperation(a, b, operation) {
  return operation(a, b);
}

const result = applyOperation(5, 2, (a, b) => a * b);
console.log(result); // Output: 10


```
