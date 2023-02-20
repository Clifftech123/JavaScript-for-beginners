## Variables and data types

Variables are used to store data in computer programs. In programming, a variable is a named container that holds a value of a particular data type. The data type determines the kind of data that can be stored in a variable and what operations can be performed on it.

In JavaScript, variables are declared using the var, let, or const keywords, followed by the variable name. The var keyword has been traditionally used in JavaScript to declare variables, but the let and const keywords were introduced in ES6 and provide more control over variable scoping and immutability, respectively.

**JavaScript has several built-in data types, including:**

| Data Types | Description | Example 
| --------    | -------- |     -------- | 
| Strings | integers and floating-point numbers | 1,2,3,4,5,6,7,8,9 
| Numbers | sequences of characters | Hello Clifford 
| BigInt | An integer with arbitrary precision |900719925124740999n , 1n etc.
| Booleans | values that can be either true or false | true, false
| Null | A value representing nothing | null
| Undefined | A value representing an uninitialized variable |  undefined
| Symbol | Data type whose instances are unique and immutable|  let value = Symbol('hello');
| Objects | Collections of key-value pairs |   {name: "Clifford", age: 25}
| Arrays | Ordered collections of value |  [1, 2, 3, "four" , "javascript"]

Here, all data types except Object are primitive data types, whereas Object and Array is non-primitive.



**JavaScript String**
String is used to store text. In JavaScript, strings are surrounded by quotes:
- Single quotes: 'Hello'
- Double quotes: "Hello"
- Backticks: ``

For Example:

```javascript
// String Example
const Single-quotes = 'Hello , This  single quote in javascript'
const DoubleQuotes = " Hello, This double quote in javascript"
const Name = Clifford
const  Backticks =` Hello, ${Name} This  is Backticks in javascript`


```
Single quotes and double quotes are practically the same and you can use either of them.Backticks are generally used when you need to include variables or expressions into a string. This is done by wrapping variables or expressions with ${variable or expression} as shown above.


**JavaScript Number**

Number represents integer and floating numbers (decimals and exponential).

For example
```javascript
// Number Example 
const number1 = 2;
const number2 = 2.433;
const number3 = 3e5 // 3 * 10^5

```
A number type can also be +Infinity, -Infinity, and NaN (not a number).

- Infinity: Represents positive infinity, which is a value greater than any other number.
-  Infinity: Represents negative infinity, which is a value less than any other number.
- NaN: (Not a Number): Represents a value that is not a legal number.

 For example,

 ```javascript
 const number1 = 3/0;
console.log(number1); // Infinity

const number2 = -3/0;
console.log(number2); // -Infinity

// strings can't be divided by numbers
const number3 = "abc"/3; 
console.log(number3);  // NaN

 ```
It's important to note that arithmetic operations with these special number values can sometimes produce unexpected results. For example, NaN is contagious, meaning that if you perform any operation with NaN, the result will also be NaN. Additionally, dividing a non-zero number by Infinity will result in zero, and dividing zero by Infinity will result in NaN. Therefore, it's important to handle these special values with care in your JavaScript code.


**JavaScript  BigInt**

In JavaScript, BigInt is a built-in numeric data type that represents integers with arbitrary precision. It allows you to work with very large numbers that are too big to be represented by the regular Number type. BigInt values are represented with the **n** suffix, like this: 12345678901234567890n.

Here's an example of using BigInt to perform arithmetic with large integers:

```javascript
const a = 12345678901234567890n;
const b = 98765432109876543210n;
const c = a + b;

console.log(c); // Outputs "111111111111111111100n"

```

In this example, we're adding two BigInt values together to get a third BigInt value. Note that the result is also a BigInt, and it has the n suffix to indicate that it is a BigInt value.

One thing to keep in mind when working with BigInt is that you cannot mix BigInt and regular Number values in arithmetic operations. For example, this code will not work as expected:

```javascript
const a = 12345678901234567890n;
const b = 123;

const c = a + b; // This will result in an error!


```
In this example, we're trying to add a BigInt value and a regular Number value together. This will result in an error, because BigInt and Number cannot be mixed in arithmetic operations.

To avoid this error, you should always use BigInt values throughout your arithmetic operations if you need to work with very large numbers.

Also, it's worth noting that BigInt is a relatively new addition to JavaScript (as of ES2020), and it may not be supported in all web browsers or environments. Be sure to check the compatibility of BigInt before using it in your project.



**JavaScript Boolean**
In JavaScript, Boolean is a primitive data type that represents a logical value, either true or false.

Boolean values are commonly used in programming to make decisions based on whether a certain condition is true or false. For example, you might use a Boolean variable to store whether a user is logged in to a website or not, or to determine whether a certain input field has been filled out by the user.

In JavaScript, you can create Boolean values using the keywords true and false.
For example

```javascript

// javascript Boolean Example
const isTrue = true;
const isFalse = false;

```
You can also use comparison operators to create Boolean values

```javascript
// javascript Boolean Example
let age = 25;
let isAdult = age >= 18; // This will evaluate to true because 25 is greater than or equal to 18


```
In addition, many JavaScript functions return Boolean values. For example, the Array.includes() method returns true if an array includes a certain value, and false otherwise:

for example

```javascript
// javascript Boolean Example
let myArray = [1, 2, 3, 4];
let includesTwo = myArray.includes(2); // This will evaluate to true
let includesFive = myArray.includes(5); // This will evaluate to false
```


**JavaScript Null**

In JavaScript, null is a primitive data type that represents the intentional absence of any object value. It is often used to indicate that a variable or object does not currently have a value, or to reset a value to null when it is no longer needed.

In JavaScript, null is represented by the keyword null. For example:

```javascript
// javascript Null Example
const nullValue = null;

```

The null value can also be used to check whether a variable or object has a value or not. For example, if you have a variable that might be empty or null, you can check it using an if statement:

```javascript
// javascript Null Example
let myVariable = null;

if (myVariable === null) {
  console.log("The variable is null");
} else {
  console.log("The variable has a value");
}

}

```

It is important to note that null is different from undefined in JavaScript. undefined means a variable has been declared but has not been assigned a value, while null represents an explicitly assigned empty value. For example:

```javascript
let myVariable;

console.log(myVariable); // This will output 'undefined'

myVariable = null;

console.log(myVariable); // This will output 'null'

```
It is also important to note that null is a primitive value, not an object, and therefore it does not have properties or methods. However, you can still use the typeof operator to determine if a value is null:

```javascript

let myVariable = null;

console.log(typeof myVariable); // This will output 'object'

```

**JavaScript Undefined**

In JavaScript, undefined is a primitive data type that represents the absence of a value. It is often used to indicate that a variable or object has not yet been assigned a value.

In JavaScript, undefined is represented by the keyword undefined. For example:

```javascript
// javascript Undefined Example
const undefinedValue = undefined;
let undefinedValue2;
console.log(undefinedValue); // This will output 'undefined'

```



**JavaScript Symbol**


In JavaScript, the symbol is a primitive data type, introduced in ECMAScript 2015 (ES6). It is used to create unique identifiers that are not accessible by any other part of the program. Symbols are often used as keys in objects to ensure that the property names are unique.

Symbols are created using the Symbol() function, which returns a new unique symbol each time it is called:

```javascript

// javascript Symbol Example
const mySymbol = Symbol();
const mySymbol2 = Symbol();

console.log(mySymbol); // This will output 'Symbol()'
console.log(mySymbol2); // This will output 'Symbol()'


const symbol1 = Symbol();
const symbol2 = Symbol();

console.log(symbol1 === symbol2); // false

```

Symbols can be used as keys in objects:

```javascript

// javascript Symbol Example
const mySymbol = Symbol('My symbol');
const myObject = {};

myObject[mySymbol] = 'Hello, world!';

console.log(myObject[mySymbol]); // 'Hello, world!'

```


**JavaScript Object**
In JavaScript, an object is a data structure that allows you to store data as key-value pairs. It is a fundamental part of the language and is used extensively in web development.

Objects in JavaScript are created using curly braces {} and can contain any number of properties, which are defined as key-value pairs separated by commas. The keys in an object are always strings, while the values can be any type of data, including other objects.

Here's an example of an object with two properties:

```javascript
// javascript Object Example
const Clifford = {
  name: 'Clifford',
  age: 30,
  Profession : " Web Developer"

};

```
In this example, person is an object with three  properties: name,  Profession  and age. The value of the name and  Profession property is a string, and the value of the age property is a number.

You can access the properties of an object using dot notation or bracket notation: 

```javascript
// javascript Object Example
console.log(Clifford.name); // 'John Doe'
console.log( console.log(Clifford.Profession); // 'Web Developer'
console.log(Clifford .age ); // 30"

};
```

In addition to storing data, objects can also have methods, which are functions that are attached to the object as properties. Here's an example of an object with a method:
    
```javascript

// javascript Object Example
const person = {
  name: 'John Doe',
  age: 30,
  greet: function() {
    console.log('Hello, world!');
  }
};

person.greet(); // 'Hello, world!'

```

In this example, the greet method is a function that logs the string 'Hello, world!' to the console. The greet method is attached to the person object as a property, and can be accessed using dot notation.


**JavaScript Array**
In JavaScript, an array is a collection of values that can be of any type, including other arrays and objects. Arrays are commonly used to store lists of items, such as numbers, strings, or objects.

Arrays in JavaScript are created using square brackets [] and can contain any number of values, separated by commas. Here's an example of an array with three values:

```javascript
// javascript Array Example
const myArray = [1, 2, 3];

```

In this example, myArray is an array with three values: 1, 2, and 3. You can access the values in an array using bracket notation and the index of the value you want to access:

You  can also use the length property to get the number of values in an array:


```javascript
// javascript Array Example
console.log(myArray[0]); // 1
console.log(myArray[1]); // 2
console.log(myArray[2]); // 3

```


You can also add and remove elements from an array using built-in methods, such as push() and pop():
    
  ```javascript
const myArray = [1, 2, 3];

myArray.push(4); // adds the value 4 to the end of the array
console.log(myArray); // [1, 2, 3, 4]

myArray.pop(); // removes the last value from the array
console.log(myArray); // [1, 2, 3]

```

Arrays also have several other built-in methods for manipulating their contents, such as shift() and unshift() for adding and removing elements from the beginning of the array, and splice() for adding or removing elements at any position in the array.

Arrays are a fundamental part of JavaScript and are used extensively in web development for handling collections of data, such as the results of a database query or a list of items to display on a page.



