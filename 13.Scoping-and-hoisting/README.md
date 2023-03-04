## Scoping and Hosting

In this section, we'll look at how JavaScript handles variable scoping and function hosting. We'll also look at the difference between global and local variables, and how to use the let and const keywords to declare variables.

- _Scoping and hoisting_:
  Scoping and hoisting are two important concepts in JavaScript that affect how variables and functions are defined and used within a program. Understanding these concepts is crucial for writing efficient and effective JavaScript code.

  ## Scoping in javascript

  Scoping is the set of rules that determines where and how a variable can be accessed in a program. In JavaScript, variables can be declared at the global level or within a function. Variables declared at the global level are called global variables, and variables declared within a function are called local variables. Global variables can be accessed from anywhere within a program, while local variables can only be accessed from within the function they were declared in.

There are two types of scopes in JavaScript: Global scope and Local scope.

- _Global scope_:
  Global scope refers to the context in which variables are accessible to any part of your code. In JavaScript, global scope refers to the top-level scope, which is the outermost scope in your code. Variables declared in the global scope can be accessed from any other scope in your code.
  Here's an example:

  ```javascript
  // global variable
  var globalVar = "I'm global!"; // global variable
  ```

in javascript, variables declared with the var keyword are automatically added to the global scope. This means that if you declare a variable in the global scope, it's accessible from any other scope in your code. However, variables declared with the let and const keywords are not automatically added to the global scope. Instead, they are only accessible within the block they were declared in.

- _Local scope_:
  Local scope refers to the context in which variables are accessible only within the current scope. In JavaScript, local scope refers to the scope of a function. Variables declared in a local scope can only be accessed from within the function they were declared in.

```javascript
function myFunction() {
	// local variable
	const localVar = "I'm local!";
	let localVar2 = "I'm also local!";
}
```

In this example, localVar and localVar2 are local variables. They can only be accessed from within the myFunction function. If you try to access them from outside the function, you'll get a ReferenceError.

## Hoisting in javascript

Hoisting is a mechanism in JavaScript where variables and function declarations are moved to the top of their respective scopes during compilation. This means that you can use a variable or function before it is declared.
The following is the JavaScript lifecycle and indicative of the sequence in which variable declaration and initialization occurs.
![Hosting](/images/hositing.png)

```javascript
console.log(x); // Output: undefined
var x = 5;
```

In the above example, the variable x is declared after it is used in the console.log statement. However, JavaScript hoists the variable declaration to the top of its scope, which means that the code is interpreted as follows:

```javascript
var x;
console.log(x); // Output: undefined
x = 5;
```

This means that you can use a variable before it is declared. However, if you try to use a variable before it is declared and initialized, you'll get a ReferenceError.

```javascript
console.log(x); // Output: ReferenceError: x is not defined
let x = 5;
```

In the above example, the variable x is declared with the let keyword, which means that it is not hoisted. This means that the code is interpreted as follows:

- **Function declarations** are also hoisted in JavaScript, which means that you can use a function before it is declared.

```javascript
myFunction(); // Output: "Hello!"`
function myFunction() {
	console.log("Hello!");
}
```
  In the above example, the myFunction function is declared after it is used in the myFunction() function call. However, JavaScript hoists the function declaration to the top of its scope, which means that the code is interpreted as follows:


```javascript
function myFunction() {
  console.log("Hello, World!");
}

myFunction(); // Output: "Hello, World!"

``` 

- **Function expressions** are not hoisted in JavaScript, which means that you cannot use a function before it is declared.

```javascript
myFunction(); // Output: TypeError: myFunction is not a function
const myFunction = function () {
    console.log("Hello, World!");
};
```

In the above example, the myFunction function is defined using a function expression, which means that it is not hoisted. When the function is called before it is defined, JavaScript throws a TypeError because myFunction is not yet a function.

### Resources
You can Read further in  Below links:

- [Scoping and hoisting](https://developer.mozilla.org/en-US/docs/Glossary/Hoisting)
  

