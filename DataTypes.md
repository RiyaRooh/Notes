# Data types
## JavaScript variables can hold different data types: numbers, strings, objects and more:
```js
let length = 16;                               // Number
let lastName = "Johnson";                      // String
let x = {firstName:"John", lastName:"Doe"};    // Object
```
When adding a number and a string, JavaScript will treat the number as a string:
```js
let x = 16 + "Volvo"; // => x = 16Volvo
``` 
JavaScript evaluates expressions from left to right. Different sequences can produce different results:
```js
let x = 16 + 4 + "Volvo"; // => x = 20Volvo
let x = "Volvo" + 16 + 4; // => x = Volvo164
```
## You can use the JavaScript ```typeof``` operator to find the type of a JavaScript variable.

The ```typeof``` operator returns the type of a variable or an expression:
```js
typeof ""             // Returns "string"
typeof "John"         // Returns "string"
typeof "John Doe"     // Returns "string"
```

## `Number.isInteger()`
>- Let's you know if a value is a number by returning true/false
```js
Number.isInteger(4) // => true
Number.isInteger('dksdfh') // => false
```
## `String()`
>- Parse a number into a string
```js
String(123) // => '123'
```
## In JavaScript, a variable without a value, has the value undefined. The type is also undefined.
```js
 let car;    // Value is undefined, type is undefined
 ```
 ## An empty value has nothing to do with undefined
 An empty string has both a legal value and a type.
 ```js
 let car = "";    // The value is "", the typeof is "string"
 ```
 