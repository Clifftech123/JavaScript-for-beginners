## Variables and data types

Variables are used to store data in computer programs. In programming, a variable is a named container that holds a value of a particular data type. The data type determines the kind of data that can be stored in a variable and what operations can be performed on it.

In JavaScript, variables are declared using the var, let, or const keywords, followed by the variable name. The var keyword has been traditionally used in JavaScript to declare variables, but the let and const keywords were introduced in ES6 and provide more control over variable scoping and immutability, respectively.

**JavaScript has several built-in data types, including:**

| Data Types | Description | Example 
| --------    | -------- |     -------- | 
| `Strings | integers and floating-point numbers | 1,2,3,4,5,6,7,8,9 
| Numbers | sequences of characters | Hello Clifford 
| BigInt | An integer with arbitrary precision |900719925124740999n , 1n etc.
| Booleans | values that can be either true or false | true, false
| Null | A value representing nothing | null
| Undefined | A value representing an uninitialized variable |  undefined
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
