### Prototype and inheritance in javascript

Prototypal inheritance is a key feature of JavaScript that allows objects to inherit properties and methods from other objects. In JavaScript, every object has an internal [[Prototype]] property, which can be thought of as a reference to another object. When a property or method is accessed on an object and it's not found on the object itself, JavaScript will look up the prototype chain to find it on the object's prototype or one of its ancestors.

Here's an example:

```javascript
var person = {
  firstName: "John",
  lastName: "Doe",
  fullName: function() {
    return this.firstName + " " + this.lastName;
  }
};

var employee = {
  jobTitle: "Developer"
};

employee.__proto__ = person;

console.log(employee.fullName()); // output: "John Doe"


```

In this example, person is an object with properties firstName, lastName, and fullName. employee is another object with a property jobTitle. The __proto__ property of employee is set to person, which means that employee inherits all of person's properties and methods.

When employee.fullName() is called, JavaScript first looks for the fullName property on employee, but it's not found. So it looks up the prototype chain to person, where it finds the fullName method. The this keyword inside the fullName method refers to employee, because that's the object the method is being called on.


One thing to note is that while __proto__ is supported in all major browsers, it's not part of the official JavaScript specification. Instead, you can use the Object.create method to create an object with a specified prototype:

```javascript

var employee = Object.create(person);
employee.jobTitle = "Developer";

```

In this example, employee is created using Object.create(person), which sets the prototype of employee to person. The jobTitle property is then added to employee.

Prototypal inheritance is a powerful and flexible way to organize and reuse code in JavaScript. By defining common properties and methods on a prototype, you can create a hierarchy of objects that share behavior and functionality.

There's also a related concept in JavaScript called classical inheritance, which emulates the class-based inheritance found in languages like Java or C++. However, classical inheritance in JavaScript is based on prototypal inheritance under the hood, and it can be less flexible and more verbose than prototypal inheritance. Some frameworks like ES6 classes and TypeScript add syntax sugar over classical inheritance for programmers who are more familiar with class-based inheritance.

Overall, understanding prototypal inheritance is essential for writing effective and maintainable JavaScript code. By using prototypes and inheritance effectively, you can create reusable, modular code that's easy to reason about and extend.
