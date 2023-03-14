## Higher order functions in javascript

### What is a higher order function?

In JavaScript, a higher order function is a function that takes one or more functions as arguments or returns a function as its result. This makes it possible to create more flexible and reusable code.

Here are some examples of higher order functions in JavaScript:

- map()

The map() function is used to apply a function to each element in an array and return a new array with the results. Here's an example:

```js
const numbers = [1, 2, 3, 4, 5];

const doubled = numbers.map((number) => number * 2);

console.log(doubled); // [2, 4, 6, 8, 10]
```

in the above example, the map() function is used to apply the function number => number \* 2 to each element in the numbers array. The result is a new array with the doubled values.

- filter()

The filter() function is used to filter out elements from an array that don't meet a certain condition. Here's an example:

```js
const numbers = [
  1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 12, 13, 14, 15, 16, 17, 18, 19, 20,
];

const even = numbers.filter((number) => number % 2 === 0);

console.log(even); // [2, 4, 6, 8, 10]
```

in the above example, the filter() function is used to filter out the odd numbers from the numbers array. The result is a new array with the even numbers.

 - reduce()

The reduce() function is used to reduce an array to a single value by applying a function to each element in the array.

    Here's an example:

```js
const numbers = [1, 2, 3, 4, 5];

const sum = numbers.reduce((total, number) => total + number, 0);

console.log(sum); // 15
```


in the above example, the reduce() function is used to sum all the numbers in the numbers array. The result is a single value.


- forEach()

The forEach() function is used to apply a function to each element in an array. Here's an example:

```js

const numbers = [1, 2, 3, 4, 5];
const numberAdd = 2 

numbers.forEach((number) =>  number * numberAdd);
console.log(numbers); // [2, 4, 6, 8, 10]
```



in the above example, the forEach() function is used to apply the function number => number \* 2 to each element in the numbers array. The result is a new array with the doubled values.


- every()

The every() function is used to check if all elements in an array meet a certain condition. Here's an example:

```js

const numbers = [1, 2, 3, 4, 5];

const allEven = numbers.every((number) => number % 2 === 0);

console.log(allEven); // false
```


in the above example, the every() function is used to check if all the numbers in the numbers array are even. The result is a boolean value.


- some()

The some() function is used to check if at least one element in an array meets a certain condition. Here's an example:

```js

const numbers = [1, 2, 3, 4, 5];

const someEven = numbers.some((number) => number % 2 === 0);

console.log(someEven); // true
```



in the above example, the some() function is used to check if at least one of the numbers in the numbers array is even. The result is a boolean value.


- find()

The find() function is used to find the first element in an array that meets a certain condition. Here's an example:

```js

const numbers = [1, 2, 3, 4, 5];

const firstEven = numbers.find((number) => number % 2 === 0);

console.log(firstEven); // 2
```


in the above example, the find() function is used to find the first even number in the numbers array. The result is the first even number.


- findIndex()

The findIndex() function is used to find the index of the first element in an array that meets a certain condition. Here's an example:

```js

const numbers = [1, 2, 3, 4, 5];

const firstEvenIndex = numbers.findIndex((number) => number % 2 === 0);

console.log(firstEvenIndex); // 1
```


in the above example, the findIndex() function is used to find the index of the first even number in the numbers array. The result is the index of the first even number.



### Why use higher order functions?

Higher order functions are useful because they allow you to create more flexible and reusable code. Here are some examples of how you can use higher order functions to create more flexible and reusable code:

- You can use the map() function to apply a function to each element in an array and return a new array with the results. This makes it possible to create a function that returns a new array with the doubled values of the numbers in an array:



You can read more about  higher oder functions in javascrpt at below link


## Resources

- [freecodecamp](https://www.freecodecamp.org/news/higher-order-functions-in-javascript-d9101f9cf528/)

- [javascript.info](https://javascript.info/higher-order-functions)

- [javascripttutorial.net](https://www.javascripttutorial.net/javascript-higher-order-functions/)
