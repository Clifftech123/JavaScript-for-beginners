
# Operators and expressions #

In computer programming, operators and expressions are used to perform various calculations and manipulations on data.
Operators are symbols or keywords used to perform operations on one or more operands (values or variables). Some common operators include*
**What is an Operator?**

In JavaScript, an operator is a special symbol used to perform operations on operands (values and variables). For example,
```javascript
2 + 3  // the + operator is used to add two numbers (2 and 3) and the result is 5

```

### JavaScript Operator Types ###

JavaScript has the following types of operators:

* **Arithmetic Operators** - used to perform arithmetic on numbers (addition, subtraction, multiplication, etc.)
* **Assignment Operators** - used to assign values to variables (equal, add and assign, subtract and assign, etc.) 
* **Comparison Operators** - used to compare two values (equal, greater than, less than, etc.)
* **Logical Operators** - used to determine the logic between variables or values (AND, OR, NOT, etc.)
* **String Operators** - used to concatenate two strings (addition, addition assignment, etc.)
* **Conditional (Ternary) Operator** - used as a shortcut for the if statement (ternary if, else if, else)
* **Bitwise Operators** - used to perform bitwise operations on numbers (AND, OR, XOR, NOT, etc.) 
  
  
In JavaScript, arithmetic operators are used to perform mathematical operations on numerical values. Here are some common arithmetic operators in JavaScript:



**Arithmetic Operators**

* Addition Operator (+)
The addition operator adds two or more numbers.
Example:
```javascript
let x = 10;
let y = 20;
let z = x + y;
console.log(z)  // the result is 30  


// Example 2
let x = 5;
let y = 20;
let z = y + x;
console.log(z)  // the result is 25 
```


* Subtraction Operator (-)
The subtraction operator subtracts one number from another.
Example:
```javascript
// Subtraction Operator (-) example
let x = 10;
let y = 20;
let z = x - y;
console.log(z)  // the result is -10  


// Example 2 
let x = 5;
let y = 20;
let z = y - x;
console.log(z)  // the result is 15 
```


* Multiplication Operator (*)
The multiplication operator multiplies two or more numbers.
Example:
```javascript
// Multiplication Operator (*) example
let x = 2;
let y = 2;
let z = x * y;
console.log(z)  // the result is  4  


// Example 2
let x = 5;
let y = 20;
let z = y * x;
console.log(z)  // the result is 100 
```


* Division Operator (/)
The division operator divides one number by another.
Example:
```javascript
// Division Operator (/) example
let x = 10;
let y = 2;
let z = x / y;
console.log(z)  // the result is 5  

// example 2
let x = 5;
let y = 20;
let z = y / x;
console.log(z)  // the result is 4 
```

* Modulus Operator or  Remainder Operator (%)
  The modulus operator returns the remainder of a division operation.
Example:
```javascript
// Modulus Operator (%) example
let x = 10;
let y = 2;
let z = x % y;
console.log(z)  // the result is 0  the remainder of 10 / 2 is 0  

// example 2
let x = 5;
let y = 21;
let z = y % x;

console.log(z)  // the result is 1  the remainder of 21 / 5 is 1 
```

* Increment Operator (++)
The increment operator increases a number by 1.
Example:
```javascript
// Increment Operator (++) example
let x = 10;
x++;
console.log(x)  // the result is 11  the value of x is increased by 1  

// example 2
let x = 5;
x++;
console.log(x)  // the result is 6  the value of x is increased by 1 
```

* Decrement Operator (--)
The decrement operator decreases a number by 1.
Example:
```javascript
// Decrement Operator (--) example
let x = 10;
x--;
console.log(x)  // the result is 9  the value of x is decreased by 1  

// example 2
let x = 5;
x--;
console.log(x)  // the result is 4  the value of x is decreased by 1 
```

**Assignment Operators**
In JavaScript, assignment operators are used to assign values to variables. Here are some common assignment operators in JavaScript:

* Simple Assignment Operator (=)
The simple assignment operator assigns a value to a variable.
Example:
```javascript
// Simple Assignment Operator (=) example
let x = 10;
console.log(x)  // the result is 10  


// example 2
let x = 5;
console.log(x)  // the result is 5 
```

* Addition Assignment Operator (+=)
  The addition assignment operator adds a value to a variable and assigns the result to the variable.
Example:
```javascript
// Addition Assignment Operator (+=) example
let x = 10;
x += 5;
console.log(x)  // the result is 15  the value of x is increased by 5  

// example 2
let x = 5;
x += 5;
console.log(x)  // the result is 10  the value of x is increased by 5 
```


* Subtraction Assignment Operator (-=)
  The subtraction assignment operator subtracts a value from a variable and assigns the result to the variable.
Example:
```javascript
// Subtraction Assignment Operator (-=) example
let x = 10;
x -= 5;
console.log(x)  // the result is 5  the value of x is decreased by 5  

// example 2
let x = 5;
x -= 5;
console.log(x)  // the result is 0  the value of x is decreased by 5 
```

* Multiplication Assignment Operator (*=)
  The multiplication assignment operator multiplies a variable by a value and assigns the result to the variable.
Example:
```javascript
// Multiplication Assignment Operator (*=) example
let x = 10;
x *= 5;
console.log(x)  // the result is 50  the value of x is multiplied by 5  

// example 2
let x = 5;
x *= 5;
console.log(x)  // the result is 25  the value of x is multiplied by 5 
```

* Division Assignment Operator (/=)
  The division assignment operator divides a variable by a value and assigns the result to the variable.
Example:
```javascript
// Division Assignment Operator (/=) example
let x = 10;
x /= 5;
console.log(x)  // the result is 2  the value of x is divided by 5  

// example 2
let x = 5;
x /= 5;
console.log(x)  // the result is 1  the value of x is divided by 5 
```

* Remainder Assignment Operator (%=)
  The remainder assignment operator divides a variable by a value and assigns the remainder to the variable.
Example:
```javascript
// Remainder Assignment Operator (%=) example
let x = 10;
x %= 5;
console.log(x)  // the result is 0  the remainder of 10 / 5 is 0  

// example 2
let a = 10;
a %= 3; // equivalent to a = a % 3;
console.log(a);    
// the result is 1  the remainder of 10 / 3 is 1 
```
 Note  : The commonly used assignment operator is =. You will understand other assignment operators such as +=, -=, *= etc. once we learn arithmetic operators.

**Comparison Operators**
In JavaScript, comparison operators are used to compare two values. 
Here are some common comparison operators in JavaScript:

* Equal to Operator (==)
The equal to operator compares two values and returns true if they are equal.
Example:
```javascript
// Equal to Operator (==) example
let x = 10;
let y = 10;
console.log(x == y)  // the result is true  

// example 2
let x = 5;
let y = 20;
console.log(x == y)  // the result is false  
```

* Not Equal to Operator (!=)
  The not equal to operator compares two values and returns true if they are not equal.
Example:
```javascript
// Not Equal to Operator (!=) example
let x = 10;
let y = 10;
console.log(x != y)  // the result is false  

// example 2
let x = 5;
let y = 20;
console.log(x != y)  // the result is true  
```

* Strict Equal to Operator (===)
 The strict equal to operator compares two values for equality, but also checks the data type of the values.
Example:
```javascript
// Strict Equal to Operator (===) example
let x = 10;
let y = 10;
console.log(x === y)  // the result is true because  both x and y are numbers  

// example 2
let x = 5;
let y = '5';
console.log(x === y)  // the result is false because  x is a number and y is a string  
```

* Strict Not Equal to Operator (!==)
  The strict not equal to operator compares two values for inequality, but also checks the data type of the values.
Example:
```javascript
// Strict Not Equal to Operator (!==) example
let x = 10;
let y = 10;
console.log(x !== y)  // the result is false because  both x and y are numbers  

// example 2
let x = 5;
let y = '5';
console.log(x !== y)  // the result is true because  x is a number and y is a string  
```

* Greater than Operator (>)
  The greater than operator compares two values and returns true if the value on the left is greater than the value on the right.
Example:
```javascript
// Greater than Operator (>) example
let x = 10;
let y = 5;
console.log(x > y)  // the result is true  

// example 2
let x = 5;
let y = 20;
console.log(x > y)  // the result is false  
``` 

* Less than Operator (<)
  The less than operator compares two values and returns true if the value on the left is less than the value on the right.
Example:
```javascript
// Less than Operator (<) example
let x = 10;
let y = 5;
console.log(x < y)  // the result is false  

// example 2
let x = 10;
let y = 40;
console.log(x < y)  // the result is true  
```

* Greater than or Equal to Operator (>=)
  The greater than or equal to operator compares two values and returns true if the value on the left is greater than or equal to the value on the right.
Example:
```javascript
// Greater than or Equal to Operator (>=) example
let x = 10;
let y = 10;
console.log(x >= y)  // the result is true because  both x and y are equal  

// example 2
let x = 5;
let y = 20;
console.log(x >= y)  // the result is false  because both x and y are equal
```

* Less than or Equal to Operator (<=)
  The less than or equal to operator compares two values and returns true if the value on the left is less than or equal to the value on the right.

Example:
```javascript
// Less than or Equal to Operator (<=) example
let x = 20;
let y = 20;
console.log(x <= y)  // the result is true because  both x and y are equal  

// example 2
let x = 50;
let y = 20;
console.log(x <= y) // the result is false because  x is  greater than y

```

**Logical Operators**
Logical operators perform logical operations and return a boolean value, either true or false. 
* Logical AND  (&& operator): It returns true if both operands are true, and false otherwise.
Example:
```javascript
// Logical AND  (&& operator) example
let x = 10;
let y = 20;
console.log(x < y && y > x)  // the result is true because both x and y are true

// example 2
let x = 10;
let y = 30;
console.log(x < y && y < x)  // the result is false because y is false
```

* Logical OR (|| operator): It returns true if either of the operands is true, and false otherwise.
  
Example:
```javascript
// Logical OR (|| operator) example
let x = 10;
let y = 20;
console.log(x < y || y > x)  // the result is true because x is true

// example 2
let x = 30;
let y = 5;
console.log(x < y || x < y)   //   the result is false because both x and y are false

```

* Logical NOT (! operator): It returns the opposite of the operand. If the operand is true, it returns false, and if the operand is false, it returns true.

Example:
```javascript
// Logical NOT (! operator) example
let a = true;
console.log(!a); // Output: false because a is true

// example 2
let b = false;
console.log(!b); // Output: true because b is false
```

**String Operators** 
JavaScript provides several string operators that can be used to manipulate and concatenate strings:

* Concatenation Operator (+): It is used to concatenate two strings. It returns a new string that is the combination of the two strings.
  
Example:
```javascript
// Concatenation Operator (+) example
let firstName = 'Isaiah';
let lastName = 'Clifford';
console.log(firstName + ' ' + lastName); // Output:  Isaiah Clifford
```

*(Compound concatenation assignment operator) (+=): It is used to concatenate a string to the end of another string. It returns a new string that is the combination of the two strings.

Example:
```javascript
// (Compound concatenation assignment operator) (+=) example
let firstName = 'Isaiah';
let lastName = 'Clifford';
firstName += ' ' + lastName;
console.log(firstName); // Output:  Isaiah Clifford
```

*Strict equality operator (===):  This operator is used to compare two strings for strict equality. It returns true if the two strings are equal, and false otherwise.

Example:
```javascript
// Strict equality operator (===) example
let firstName = 'Isaiah';
let lastName = 'Clifford';
console.log(firstName === lastName); // Output:  false because the two strings are not equal

// example 2
let firstName = 'Isaiah';
let lastName = 'Isaiah';
console.log(firstName === lastName); // Output:  true because the two strings are equal

```

*Strict inequality operator (!==):  This operator is used to compare two strings for strict inequality. It returns true if the two strings are not equal, and false otherwise.

Example:
```javascript
// Strict inequality operator (!==) example
let firstName = 'Isaiah';
let lastName = 'Clifford';
console.log(firstName !== lastName); // Output:  true because the two strings are not equal


// example 2
let firstName = 'Isaiah';
let lastName = 'Isaiah';
console.log(firstName !== lastName); // Output:  false because the two strings are equal

```


**Conditional (Ternary) Operator**
The conditional operator is the only JavaScript operator that takes three operands. The operator can have one of two values based on a condition. The syntax is as follows:
```javascript
condition ? value1 : value2
```
The condition is evaluated. If it’s truthy, value1 is returned, otherwise, value2 is returned.

Here's an example:
```javascript
// Conditional (Ternary) Operator example
let age = 20;
let isAdult = age >= 18 ? "Yes" : "No";
console.log(isAdult); // Output: Yes Because age is greater than or equal to 18
//In this example, if the age is greater than or equal to 18, the value of isAdult will be "Yes", otherwise it will be "No"

// example 2

let age = 10;
let isAdult = age >= 18 ? "Yes" : "No";
console.log(isAdult); // Output: No Because age is less than 18

```
The conditional operator can be used to assign values or execute functions based on a condition in a more concise way than using an if-else statement. However, it can also make the code harder to read if it is overused or if the expressions are too complex. Therefore, it is important to use the conditional operator judiciously and only when it makes the code clearer and more concise.

**Bitwise Operators**
Bitwise operators perform operations on binary representations of numbers.JavaScript provides six bitwise operators that allow you to manipulate the binary representation of numbers at the bit level.

* Bitwise AND (&): It returns a number where the bits of that number are set to 1 if the corresponding bits of both numbers are 1. Otherwise, it returns 0.
  
Example:
```javascript
// Bitwise AND (&) example
let a = 5; // binary: 0101
let b = 3; // binary: 0011
console.log(a & b); // Output: 1 (binary: 0001)
// example 2

let a = 5; // binary: 0101
let b = 7; // binary: 0111
console.log(a & b); // Output: 5 (binary: 0101)

```

* Bitwise OR (|): It returns a number where the bits of that number are set to 1 if the corresponding bits of either of the two numbers are 1. Otherwise, it returns 0.
  
Example:
```javascript
// Bitwise OR (|) example
let a = 5; // binary: 0101
let b = 3; // binary: 0011
console.log(a | b); // Output: 7 (binary: 0111)

// example 2
let a = 5; // binary: 0101
let b = 7; // binary: 0111
console.log(a | b); // Output: 7 (binary: 0111)

```

* Bitwise XOR (^): It returns a number where the bits of that number are set to 1 if the corresponding bits of either of the two numbers are 1, but not both. Otherwise, it returns 0.
  
Example:
```javascript
// Bitwise XOR (^) example
let a = 5; // binary: 0101
let b = 3; // binary: 0011
console.log(a ^ b); // Output: 6 (binary: 0110)

```

* Bitwise NOT (~): It returns a number where the bits of that number are flipped. It returns the one’s complement of the number.
  
  Example 

  ```javascript
  // Bitwise NOT (~) example
    let a = 5; // binary: 0101
    console.log(~a); // Output: -6 (binary: 1010)
   ```


* Left shift (<<): It returns a number where the bits of the first number are shifted to the left by the number of places specified by the second number. The bits shifted out of the left side of the number are discarded. The bits shifted in on the right side are filled with 0.


Example:
```javascript

// Left shift (<<) example
let a = 5; // binary: 0101
console.log(a << 1); // Output: 10 (binary: 1010)
```

* Right shift (>>): It returns a number where the bits of the first number are shifted to the right by the number of places specified by the second number. The bits shifted out of the right side of the number are discarded. The bits shifted in on the left side are filled with 0.

Example:
```javascript
// Right shift (>>) example
let a = 5; // binary: 0101
console.log(a >> 1); // Output: 2 (binary: 0010)
```
