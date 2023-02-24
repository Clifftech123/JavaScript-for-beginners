## JavaScript Objects ## 


**What is a JavaScript Object?**
In JavaScript, an object is a collection of properties, where each property consists of a key and a value. The key is a string that represents the name of the property, and the value can be any valid JavaScript value, including other objects.


Creating a JavaScript Object:
There are several ways to create a JavaScript object. One of the most common ways is to use object literal notation, which allows you to define an object by enclosing a comma-separated list of key-value pairs in curly braces.

Here is an example of creating an object using object literal notation:

 ```javascript
 let myObject = {
   name : "John",
    age : 30,
    city : "New York"


};
  
```
 Accessing Object Properties: 
You can access the properties of an object using the dot notation or the bracket notation. The dot notation is used when you know the name of the property you want to access. The bracket notation is used when you want to access a property using a variable.

Here is an example of accessing an object property using the dot notation:

```javascript
let myObject = {
  name : "John",
  age : 30,
  city : "New York"
};

// Accessing object properties using the dot notation
console.log(myObject.name); // outPut: John
console.log(myObject.age); // output: 30
console.log(myObject.city); // output: New York


// Accessing object properties using the bracket notation
console.log(myObject["name"]); // outPut: John
console.log(myObject["age"]); // output: 30
console.log(myObject["city"]); // output : New York


```

**Adding New Properties to an Object:**
You can add new properties to an object by using the dot notation or the bracket notation. The dot notation is used when you know the name of the property you want to add. The bracket notation is used when you want to add a property using a variable.

Here is an example of adding a new property to an object using the dot notation:

```javascript
let myObject = {
  name : "John",
  age : 30,
  city : "New York"
};

// Adding a new property to an object using the dot notation
myObject.country = "USA";
console.log(myObject.country); // output: USA

myObject["age"] = "50"; 
console.log(myObject.age); // output: 50

myObject["name"] = "Clifford"; 
console.log(myObject.name); // output:  Clifford


// Adding a new property to an object using the bracket notation
myObject["country"] = "UK";
console.log(myObject.country); // output: UK

myObject["age"] = "60";
console.log(myObject.age); // output: 60


myObject["name"] = "Isaiah";
console.log(myObject.name); // output: Isaiah

```


**Deleting Properties from an Object:**
You can delete properties from an object by using the delete operator.

Here is an example of deleting a property from an object:

```javascript
let myObject = {
  name : "John",
  age : 30,
  city : "New York"
};

// Deleting a property from an object

delete myObject.city;
console.log(myObject.city); // output: undefined

console.log(myObject); // output: {name: "John", age: 30}

 // now we are getting a new object with only 2 properties because  the city property was deleted

```

**Looping Through an Object:**
You can loop through the properties of an object using the for...in loop.

Here is an example of looping through an object:

```javascript
let myObject = {
  name : "John",
  age : 30,
  city : "New York"
};

// Looping through an object
for (let key in myObject) {
  console.log(key + " : " + myObject[key]);
}

// output: name : John 
// output: age : 30
// output: city : New York

```


Conclusion:
In summary, JavaScript objects are a powerful tool for storing and manipulating data in web development. They allow you to create complex data structures and access properties using dot notation or bracket notation. By mastering the concepts of JavaScript objects, you will be well on your way to becoming a proficient web developer.



