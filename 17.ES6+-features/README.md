## Javascript ES6+ features

- **What is ES6?**
  ES6 or the ECMAScript 2015 is the 6th and major edition of the ECMAScript language specification standard. It defines the standard for the implementation of JavaScript and it has become much more popular than the previous edition ES5.

ES6 comes with significant changes to the JavaScript language. It brought several new features like, let and const keyword, rest and spread operators, template literals, classes, modules and many other enhancements to make JavaScript programming easier and more fun. In this article, we will discuss some of the best and most popular ES6 features that we can use in your everyday JavaScript coding.

let take a look at some of the most popular ES6 features.

- **let and const**
  The let and const keywords are used to declare variables in ES6. The let keyword is used to declare a variable that can be reassigned later in the program. The const keyword is used to declare a variable that cannot be reassigned later in the program.

```js
let name = "Clifford";
name = "Isaiah";
console.log(name); // Isaiah

// let and const are block scoped
// let can be redeclare
// let must be initialized during declaration
// let can be object but cant be reassigned

const age = 25;
age = 30; // TypeError: Assignment to constant variable.

// let and const are block scoped
// const cant be redeclare
// const must be initialized during declaration
// const can be object but cant be reassigned
```

- **Arrow functions**
  Arrow functions are a new way to write functions in ES6. Arrow functions are a shorter way to write functions in JavaScript. Arrow functions are always anonymous. They cannot be named. Arrow functions are also called fat arrow functions.

```js
// Define a function using the arrow function syntax
const myFunction = (name) => {
  console.log(`Hello, ${name}!`);
};

myFunction("Alice"); // Output: "Hello, Alice!"

// ES5
function add(a, b) {
  return a + b;
}

add(1, 2); // 3
// ES6

const add = (a, b) => {
  return a + b;
};
add(4, 2); // 6

// ES6
const add = (a, b) => a + b;

add(4, 2); // 6

// ES6

// if the function has only one parameter, you can omit the parentheses
// if the function has only one statement, you can omit the curly braces and the return keyword
// if the function has no parameter, you must include the parentheses
```

- **Template literals**
  Template literals are a new way to create strings in ES6. Template literals are enclosed by backticks (`) instead of single or double quotes. Template literals can contain placeholders. These are indicated by the dollar sign and curly braces (${expression}).

```js
// Use template literals to create a multiline string with variables
const name = "Bob";
const age = 42;
const greeting = `Hello, my name is ${name} and I am ${age} years old.`;
console.log(greeting); // Output: "Hello, my name is Bob and I am 42 years old."

// ES5
var name = "Clifford";
var age = 25;
var message = "Hello, my name is " + name + " and I am " + age + " years old.";
console.log(message); // Output: "Hello, my name is Clifford and I am 25 years old."

// ES6

const name = "Clifford";
const age = 25;
const message = `Hello, my name is ${name} and I am ${age} years old.`;

console.log(message); // Output: "Hello, my name is Clifford and I am 25 years old."

//  Template literals can contain placeholders. These are indicated by the dollar sign and curly braces (${expression}).
// Template literals are enclosed by backticks (`) instead of single or double quotes.
```

- **Destructuring**
  Destructuring is a new way to extract data from arrays and objects in ES6. Destructuring is a convenient way to extract data from arrays and objects. It allows you to assign the values of an array or object to variables in a single line of code.

```js
// Destructuring arrays
const names = ["Alice", "Bob", "Charlie", "Dave"];
const [name1, name2, name3, name4] = names;
console.log(name1); // Output: "Alice"

// Destructuring objects

const person = {
  name: "Alice",
  age: 25,
  address: {
    city: "New York",
    state: "NY",
  },
};

const { name, age, address } = person;
console.log(name); // Output: "Alice"
console.log(age); // Output: 25
console.log(address); // Output: {city: "New York", state: "NY"}

// Destructuring nested objects

const person = {
  name: "Alice",
  age: 25,
  address: {
    city: "New York",
    state: "NY",
  },
};

const {
  name,
  age,
  address: { city, state },
} = person;

console.log(name); // Output: "Alice"
console.log(age); // Output: 25
console.log(city); // Output: "New York"
console.log(state); // Output: "NY"

//  destructuring is a convenient way to extract data from arrays and objects. It allows you to assign the values of an array or object to variables in a single line of code.
```

- **Rest and spread operators**
  The rest and spread operators are used to work with arrays in ES6. The rest operator allows you to represent an indefinite number of arguments as an array. The spread operator allows you to expand an array into its elements.

```js
// Use the rest operator to represent an indefinite number of arguments as an array

function sum(...numbers) {
  return numbers.reduce((total, number) => total + number, 0);
}

console.log(sum(1, 2, 3, 4, 5)); // Output: 15

// Use the spread operator to expand an array into its elements

const numbers = [1, 2, 3, 4, 5];

console.log(...numbers); // Output: 1 2 3 4 5

// The rest operator allows you to represent an indefinite number of arguments as an array.

// The spread operator allows you to expand an array into its elements.
```

- **Classes**
  Classes are a new way to create objects in ES6. Classes are a template for creating objects. They encapsulate data with code to work on that data. Classes in ES6 are built on prototypes but also have some syntax and semantics that are not shared with ES5 class-like semantics.

```js


// Define a class
class Person {
  constructor(name) {
    this.name = name;
  }

  greet() {
    console.log(`Hello, my name is ${this.name}!`);
  }
}

// Create an object from a class
const person = new Person("Alice");

person.greet(); // Output: "Hello, my name is Alice!"

// Define a class
class Person {
  constructor(name) {
    this.name = name;
  }

  greet() {
    console.log(`Hello, my name is ${this.name}!`);
  }
}

// Create an object from a class
const person = new Person("Alice");

person.greet(); // Output: "Hello, my name is Alice!"

5 class-like semantics.

```

Classes are a template for creating objects. They encapsulate data with code to work on that data. Classes in ES6 are built on prototypes but also have some syntax and semantics that are not shared with ES

- **Modules**
  Modules are a new way to organize code in ES6. Modules are reusable pieces of code that can be exported from one program and imported for use in another program. Modules are declared using the export and import keywords.

```js
// Export a module
export const name = "Alice";

// Import a module
import { name } from "./module.js";

console.log(name); // Output: "Alice"

// Export a module default
export default function add(a, b) {
  return a + b;
}

// Import a module default

import add from "./module.js";

console.log(add(1, 2)); // Output: 3

// i
```

- **Promises**
  Promises are a new way to handle asynchronous operations in ES6. Promises are used to handle asynchronous operations in JavaScript. They are easy to manage when dealing with multiple asynchronous operations where callbacks can create callback hell leading to unmanageable code. A Promise has three states: pending, resolved, and rejected.

```js
// Create a promise
const promise = new Promise((resolve, reject) => {
  const number = Math.floor(Math.random() * 10);

  if (number % 2 === 0) {
    resolve(number);
  } else {
    reject(number);
  }
});

// Consume a promise

promise
  .then((number) => {
    console.log(`Success: ${number} is even.`);
  })
  .catch((number) => {
    console.log(`Error: ${number} is odd.`);
  });
```

Promises are used to handle asynchronous operations in JavaScript. They are easy to manage when dealing with multiple asynchronous operations where callbacks can create callback hell leading to unmanageable code. A Promise has three states: pending, resolved, and rejected.

- **Generators**
  Generators are a new way to create iterators in ES6. Generators are functions that can be exited and later re-entered. Their context (variable bindings) will be saved across re-entrances. Generators are declared using the function\* syntax.

```js
// Define a generator

function* idMaker() {
  let index = 0;

  while (index < 3) {
    yield index++;
  }
}

// Create an iterator from a generator

const iterator = idMaker();

console.log(iterator.next().value); // Output: 0
console.log(iterator.next().value); // Output: 1
```

Generators are functions that can be exited and later re-entered. Their context (variable bindings) will be saved across re-entrances. Generators are declared using the function\* syntax.

- **Map and Set**
  Map and Set are new data structures in ES6. Map is a collection of keyed data items, just like an Object. But the main difference is that Map allows keys of any type. Set is a collection of values, where each value may occur only once. It’s just like an Array of unique values, but the main difference is that Set doesn’t allow to store the same value twice.

```js
// Create a map

const map = new Map();

map.set("name", "Alice");
map.set("age", 25);

console.log(map.get("name")); // Output: "Alice"

// Create a set

const set = new Set();

set.add("name");
set.add("age");

console.log(set.has("name")); // Output: true
```

Map is a collection of keyed data items, just like an Object. But the main difference is that Map allows keys of any type. Set is a collection of values, where each value may occur only once. It’s just like an Array of unique values, but the main difference is that Set doesn’t allow to store the same value twice.

You can read more about ES6 in the below links:

## Resource

- [ES6](https://www.w3schools.com/js/js_es6.asp)
