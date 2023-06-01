---
title: Array Methods: .map()
publishDate: 1 June 2023
description: Delving in to the array.map() method in JS.
tags: ['js', 'arrays', 'map']
---

The `map()` method is used to create a new array by applying a function to each element of an original array. The `map()` function calls the provided function once for each element in an array, in order.

Here's an example:

```javascript
let numbers = [1, 2, 3, 4, 5];

let squares = numbers.map(num => num * num);

console.log(squares); // Output: [1, 4, 9, 16, 25]
```

In the example above, `map()` applies a function that squares each number in the `numbers` array and then creates a new `squares` array with the results. The original `numbers` array is not changed. The `map()` method does not modify the original array. Instead, it returns a new array with the results of applying the callback function to each element in the original array.

Let's see a few more examples of how to use the `Array.prototype.map()` method.

**Doubling the numbers in an array**

```javascript
let numbers = [1, 2, 3, 4, 5];

let doubled = numbers.map(num => num * 2);

console.log(doubled); // Output: [2, 4, 6, 8, 10]
```

**Changing the shape of objects in an array**

```javascript
let objects = [{id: 1, name: 'Joe'}, {id: 2, name: 'Sally'}, {id: 3, name: 'Bob'}];

let names = objects.map(obj => obj.name);

console.log(names); // Output: ['Joe', 'Sally', 'Bob']
```

**Applying a mathematical operation**

```javascript
let anglesInDegrees = [30, 45, 60, 90];

let anglesInRadians = anglesInDegrees.map(degrees => degrees * (Math.PI / 180));

console.log(anglesInRadians); // Output: [0.5235987755982988, 0.7853981633974483, 1.0471975511965976, 1.5707963267948966]
```

**Adding an index to each element**

```javascript
let fruits = ['apple', 'banana', 'mango', 'orange', 'peach'];

let indexedFruits = fruits.map((fruit, index) => `${index + 1}: ${fruit}`);

console.log(indexedFruits); // Output: ["1: apple", "2: banana", "3: mango", "4: orange", "5: peach"]
```

**Create a new array of strings to represent objects**

```javascript
let pets = [
  { type: 'Dog', name: 'Spot' },
  { type: 'Cat', name: 'Tiger' },
  { type: 'Fish', name: 'Goldie' }
];

let petDescriptions = pets.map(pet => `${pet.name} is a ${pet.type}`);

console.log(petDescriptions); // Output: ['Spot is a Dog', 'Tiger is a Cat', 'Goldie is a Fish']
```

These examples should help you understand how flexible the `Array.prototype.map()` function is and how it can be used in a variety of different situations.
