## Conditionals and loops in javascript

Conditionals and loops are essential building blocks of programming, and they are no different in JavaScript. In this answer, we'll take a closer look at how to use conditionals and loops in JavaScript.

**Conditional statements in JavaScript**
JavaScript provides two conditional statements: "if" and "switch". Here's how they work:

- if statement:
  The if statement executes a block of code if a specified condition is true.
  Here's an example:

  ```javascript
  if (condition) {
  	// code to be executed if condition is true
  	// if the condition is true, the code inside the curly braces will be executed
  }

  let age = 18;

  if (age >= 18) {
  	console.log("You are old enough to vote.");
  } else {
  	console.log("You are not old enough to vote yet.");
  }
  ```

  In this example, we have a variable "age" that is set to 18. The "if" statement checks if the value of "age" is greater than or equal to 18. If it is, it executes the code block inside the "if" statement and prints "You are old enough to vote.". Otherwise, it executes the code block inside the "else" statement and prints "You are not old enough to vote yet.

- switch statement:

  The switch statement allows you to execute different actions based on different conditions.
  Here's an example:

  ```javascript
  switch (expression) {
  	case x:
  		// code block
  		break;
  	case y:
  		// code block
  		break;
  	default:
  		// code block

  		let day = "Monday";

  		switch (day) {
  			case "Monday":
  				console.log("Today is Monday.");
  				break;
  			case "Tuesday":
  				console.log("Today is Tuesday.");
  				break;
  			case "Wednesday":
  				console.log("Today is Wednesday.");
  				break;
  			default:
  				console.log("Today is some other day.");
  		}
  }
  ```

  In this example, we have a variable "day" that is set to "Monday". The "switch" statement checks the value of "day" and executes the code block that matches the value. In this case, it prints "Today is Monday.


**Loops in JavaScript**
JavaScript provides three types of loops: "for", "while", and "do...while". Here's how they work:

- for loop:

  The for loop is used to execute a block of code a number of times.
  Here's an example:

  ```javascript
  for (statement 1; statement 2; statement 3) {
  	// code block to be executed
  }

  for (let i = 0; i < 5; i++) {
  	console.log(i); // 0, 1, 2, 3, 4
  }
  ```

  In this example, we have a variable "i" that is set to 0. The "for" loop checks if the value of "i" is less than 5. If it is, it executes the code block inside the "for" loop and prints the value of "i". Then, it increments the value of "i" by 1 and checks the condition again. This process repeats until the value of "i" is no longer less than 5.


- while loop:
  
    The while loop loops through a block of code as long as a specified condition is true.
    Here's an example:
    
    ```javascript
    while (condition) {
    	// code block to be executed
    }
    
    let i = 0;
    
    while (i < 5) {
    	console.log(i); // 0, 1, 2, 3, 4
    	i++;
    }
    ```
    
    In this example, we have a variable "i" that is set to 0. The "while" loop checks if the value of "i" is less than 5. If it is, it executes the code block inside the "while" loop and prints the value of "i". Then, it increments the value of "i" by 1 and checks the condition again. This process repeats until the value of "i" is no longer less than 5.



- do...while loop:
  
    The do...while loop is a variant of the while loop. This loop will execute the code block once, before checking if the condition is true, then it will repeat the loop as long as the condition is true.
    Here's an example:
    
    ```javascript
    do {
    	// code block to be executed
    } while (condition);
    
    let i = 0;
    
    do {
    	console.log(i); // 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
    	i++;
    } while (i < 10);
    ```
    
    In this example, we have a variable "i" that is set to 0. The "do...while" loop executes the code block inside the "do...while" loop and prints the value of "i". Then, it increments the value of "i" by 1 and checks the condition. If the condition is true, the loop repeats. This process repeats until the value of "i" is no longer less than 10.

**Conclusion**
In this answer, we took a closer look at how to use conditionals and loops in JavaScript. We learned about the "if" and "switch" statements, and the "for", "while", and "do...while" loops. We also learned how to use these statements and loops in JavaScript.


