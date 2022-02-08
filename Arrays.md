# Arrays
Arrays are often declared with `const`
> You can also create an array, and then provide the elements
```js
const cars = [];
cars[0]= "Saab";
cars[1]= "Volvo";
cars[2]= "BMW";
```
### The length Property
The length property of an array returns the length of an array (the number of array elements):
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let length = fruits.length; // => 4
```
**The length property is always one more than the highest array index**
>- Accessing the First Array Element
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let fruit = fruits[0]; // =>Banana
```
>- Accessing the Last Array Element
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let fruit = fruits[fruits.length - 1]; // => Mango
```
## `Array.forEach()` function
> Loops through an array without returning anything
## Adding Array Elements
### The easiest way to add a new element to an array is using the `push()` method
```js
const fruits = ["Banana", "Orange", "Apple"];
fruits.push("Lemon");  // Adds a new element (Lemon) to fruits
```
### New element can also be added to an array using the length property
```js
const fruits = ["Banana", "Orange", "Apple"];
fruits[fruits.length] = "Lemon";  // Adds "Lemon" to fruits
```
**WARNING !**

 *Adding elements with high indexes can create undefined "holes" in an array*
 ```js
 const fruits = ["Banana", "Orange", "Apple"];
fruits[6] = "Lemon";  // Creates undefined "holes" in fruits
```
>- JavaScript does not support arrays with named indexes.

In JavaScript, arrays always use numbered indexes
```js
const person = [];
person[0] = "John";
person[1] = "Doe";
person[2] = 46;
person.length;    // Will return 3
person[0];        // Will return "John"
```
## How to Recognize an Array
>- `Array.isArray()`
```js
const fruits = ["Banana", "Orange", "Apple"];
Array.isArray(fruits); // => true
```
>- The `instanceof` operator returns true if an object is created by a given constructor
```js
const fruits = ["Banana", "Orange", "Apple"];

fruits instanceof Array; // => true
```
## Converting Arrays to Strings
>- The JavaScript method `toString()` converts an array to a string of (comma separated) array values
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
const strfruits = fruits.toString();
```
>- The `join()` method also joins all array elements into a string

*It behaves just like `toString()`, but in addition you can specify the separator*
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
const strfruits = fruits.join("*"); // => Banana * Orange * Apple * Mango
```
## JavaScript `Array.pop()`
>- The `pop()` method removes the last element from an array
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.pop(); // => Banana,Orange,Apple
```
>- The `pop()` method returns the value that was "popped out"
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let fruit = fruits.pop(); // => Mango
```
## JavaScript `Array.push()`
>- The `push()` method adds a new element to an array (at the end)
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.push("Kiwi"); // => Banana,Orange,Apple,Mango,Kiwi
```
>- The `push()` method returns the new array length
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let length = fruits.push("Kiwi"); // => 5
```
## JavaScript `Array.shift()`
>- The `shift()` method removes the first array element and "shifts" all other elements to a lower index
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.shift(); // => Orange,Apple,Mango
```
>- The `shift()` method returns the value that was "shifted out"
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let fruit = fruits.shift(); // => Banana
```
## JavaScript `Array.unshift()`
>- The `unshift()` method adds a new element to an array (at the beginning), and "unshifts" older elements
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.unshift("Lemon"); // => Lemon,Banana,Orange,Apple,Mango
```
>- The `unshift()` method returns the new array length
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.unshift("Lemon"); // => 5
```
## Changing Elements
>- Array elements are accessed using their index number
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits[0] = "Kiwi"; // => Kiwi,Orange,Apple,Mango
```
## JavaScript Array length
>- The length property provides an easy way to append a new element to an array
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits[fruits.length] = "Kiwi"; // => Banana,Orange,Apple,Mango,Kiwi
```
## JavaScript Array delete()
**Warning !**

*Array elements can be deleted using the JavaScript operator delete.*

*Using delete leaves undefined holes in the array.*

*Use `pop()` or `shift()` instead.*
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
delete fruits[0]; // => undefined, Orange, Apple, Mango
```
## Merging (Concatenating) Arrays
>- The `concat()` method creates a new array by merging (concatenating) existing arrays
```js
const myGirls = ["Cecilie", "Lone"];
const myBoys = ["Emil", "Tobias", "Linus"];

const myChildren = myGirls.concat(myBoys); // => Cecilie,Lone,Emil,Tobias,Linus
```
>- The `concat()` method can take any number of array arguments
```js
const arr1 = ["Cecilie", "Lone"];
const arr2 = ["Emil", "Tobias", "Linus"];
const arr3 = ["Robin", "Morgan"];
const myChildren = arr1.concat(arr2, arr3); // => Cecilie,Lone,Emil,Tobias,Linus,Robin,Morgan
```  
>- The `concat()` method can also take strings as arguments
```js
const arr1 = ["Emil", "Tobias", "Linus"];
const myChildren = arr1.concat("Peter");  // => Emil,Tobias,Linus,Peter
```
## Splicing and Slicing Arrays
- The `splice()` method adds new items to an array.

- The `slice()` method slices out a piece of an array.
## JavaScript Array `splice()`
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(2, 0, "Lemon", "Kiwi"); // => Banana,Orange,Lemon,Kiwi,Apple,Mango
```
- The first parameter (2) defines the position where new elements should be added (spliced in).

- The second parameter (0) defines how many elements should be removed.

- The rest of the parameters ("Lemon" , "Kiwi") define the new elements to be added.
>- The `splice()` method returns an array with the deleted items
```js 
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(2, 2, "Lemon", "Kiwi"); // => Apple,Mango
```
## Using `splice()` to Remove Elements
>- With clever parameter setting, you can use `splice()` to remove elements without leaving "holes" in the array
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(0, 1); // => Orange,Apple,Mango
```
- The first parameter (0) defines the position where new elements should be added (spliced in).

- The second parameter (1) defines how many elements should be removed.

- The rest of the parameters are omitted. No new elements will be added.
- ## JavaScript Array `slice()`
>- The `slice()` method slices out a piece of an array into a new array.

This example slices out a part of an array starting from array element 1 ("Orange")
```js
const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
const citrus = fruits.slice(1); // => Orange,Lemon,Apple,Mango
```
This example slices out a part of an array starting from array element 3 ("Apple")
```js
const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
const citrus = fruits.slice(3); // => Apple, Mango
```
>- The `slice()` method can take two arguments like slice(1, 3).

- The method then selects elements from the start argument, and up to **(but not including)** the end argument
```js
  const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
const citrus = fruits.slice(1, 3); // => Orange,Lemon
```
>- If the end argument is omitted, like in the first examples, the `slice()` method slices out the rest of the array
```js
const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
const citrus = fruits.slice(2); // => Lemon,Apple,Mango
```
## Sorting an Array
>- The `sort()` method sorts an array alphabetically
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.sort(); // => Apple,Banana,Mango,Orange
```
>- Sort numbers in ascending order
```js
const points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return a-b});
```
>- Sort numbers in descending order
```js
const points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return b-a});
```
## Reversing an Array
>- The `reverse()` method reverses the elements in an array.

You can use it to sort an array in descending order
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.sort();
fruits.reverse(); // => Orange,Mango,Banana,Apple
```
## JavaScript Array `forEach()`
>- You call this method on your array, and pass in a callback function to run on each iteration of the loop. The callback accepts two arguments. The first is the value of the current item in the loop, and the second is the index of that item.
```js
var sandwiches = [
	'tuna',
	'ham',
	'turkey',
	'pb&j'
];

sandwiches.forEach(function (sandwich, index) {
	console.log(index);
	console.log(sandwich);
});

// returns 0, "tuna", 1, "ham", 2, "turkey", 3, "pb&j"
```
## Array `map()`
>- The `Array.map()` method creates a new array from an existing one. It loops through each item in the original array, transforms it in some way, and then pushes it into a new array. All of this happens behind-the-scenes.

For example, let’s say you had an array of numbers, and you wanted to create a new array with the numbers doubled.
```js
var numbers = [3, 11, 42];
// Create a new array of doubled numbers
var doubled = numbers.map(function (number) {
	return number * 2; // => [6, 22, 84]
});
```
## Array `fiter()`
>- Inside the `Array.filter()` callback function, return true if the item should be added to the new array, and false if it shouldn’t. Under-the-hood, `Array.filter()` loops through each item in the original array, runs your callback method on each item, creates a new array, and pushes the items that return true.
```js
var wizards = [
	{
		name: 'Harry Potter',
		house: 'Gryfindor'
	},
	{
		name: 'Cedric Diggory',
		house: 'Hufflepuff'
	},
	{
		name: 'Tonks',
		house: 'Hufflepuff'
	},
	{
		name: 'Ronald Weasley',
		house: 'Gryfindor'
	},
	{
		name: 'Hermione Granger',
		house: 'Gryfindor'
	}
]; 
// You want only Gryfindor wizards
// Create a new array from the wizard array
var gryfindor = wizards.filter(function (wizard) {
	// Only include wizards from the Gryfindor house
	if (wizard.house === 'Gryfindor') return true;
	return false;
});

OR

// Create a new array from the wizard array
var gryfindor = wizards.filter(function (wizard) {
	// Only include wizards from the Gryfindor house
	return wizard.house === 'Gryfindor';
});
```
## Array `reduce()`
>- It’s purpose is to take an array and condense it’s content into a single value. That value can be a number, a string, or even an object or new array. That’s the part that’s always tripped me up. I didn’t realize just how flexible it is!

The `Array.reduce()` accepts two arguments: a callback method to run against each item in the array, and a starting value.

The callback also accepts two arguments: the accumulator, which is the current combined value, and the current item in the loop. Whatever you return is used as the accumulator for the next item in the loop. On the very first loop, that starting value is used instead.

Here, we pass in 0 as our starting value.

In the callback, we add the current value to the sum, which has our starting value of 0 on the first loop, then 1 (the starting value of 0 plus the item value of 1), then 3 (the sum value of 1 plus the item value of 2), and so on.
```js
var total = [1, 2, 3].reduce(function (sum, current) {
	return sum + current;
}, 0); // => 6
```
## Array `every()`
>- The `every()` method tests whether all elements in the array pass the test implemented by the provided function. It returns a Boolean value.
```js
const isBelowThreshold = (currentValue) => currentValue < 40;

const array1 = [1, 30, 39, 29, 10, 13];

console.log(array1.every(isBelowThreshold));
// expected output: true
```
## Array `some()`
>- The `some()` method check if some array values pass a test. This example check if some array values are larger than 18
```js 
const numbers = [45, 4, 9, 16, 25];
let someOver18 = numbers.some(myFunction);

function myFunction(value, index, array) {
  return value > 18; // => false
}
```
## Array `includes()`
>- The `includes()` method determines whether an array includes a certain value among its entries, returning true or false as appropriate.
```js
const array1 = [1, 2, 3];

console.log(array1.includes(2));
// expected output: true

const pets = ['cat', 'dog', 'bat'];

console.log(pets.includes('cat'));
// expected output: true

console.log(pets.includes('at'));
// expected output: false
```