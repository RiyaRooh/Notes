# Numbers
> JavaScript uses the `+` operator for both addition and concatenation.Numbers are added. Strings are concatenated.
>- If you add two strings, the result will be a string concatenation
>- If you add a number and a string, the result will be a string concatenation
>- If you add a string and a number, the result will be a string concatenation
## NaN - Not a Number
`NaN` is a JavaScript reserved word indicating that a number is not a legal number.

Trying to do arithmetic with a non-numeric string will result in `NaN` (Not a Number)

`NaN` is a number: `typeof NaN` returns number
```js
typeof NaN; // => number
```
## The `toString()` Method
The `toString()` method returns a number as a string
```js
let x = 123;
x.toString(); // => 123
(123).toString(); // => 123
(100 + 23).toString(); // => 123
```
## The `toFixed()` Method
`toFixed()` returns a string, with the number written with a specified number of decimals
```js
let x = 9.656;
x.toFixed(0); // => 10
x.toFixed(2); // => 9.66
x.toFixed(4); // => 9.656
x.toFixed(6); // => 9.656000
```
## The `toPrecision()` Method
`toPrecision()` returns a string, with a number written with a specified length
```js
let x = 9.656;
x.toPrecision(); // => 9.656
x.toPrecision(2); // => 9.7
x.toPrecision(4); // => 9.656
x.toPrecision(6); // => 9.65600
```
## The `valueOf()` Method
`valueOf()` returns a number as a number
```js
let x = 123;
x.valueOf(); // => 123
(123).valueOf(); // => 123
(100 + 23).valueOf(); // => 123
```

##  Converting Variables to Numbers
> There are 3 JavaScript methods that can be used to convert variables to numbers:
>- The `Number()` method
>- The `parseInt()` method
>- The `parseFloat()` method
 ### The `Number()` Method
`Number()` can be used to convert JavaScript variables to numbers
> If the number cannot be converted, **NaN (Not a Number)** is returned
### The `parseInt()` Method
`parseInt()` parses a string and returns a whole number. Spaces are allowed. Only the first number is returned
```js
parseInt("-10"); // => -10
parseInt("-10.33"); // => -10
parseInt("10"); // => 10
parseInt("10.33"); // => 10
parseInt("10 20 30"); // => 10
parseInt("10 years"); // => 10
parseInt("years 10"); // => NaN
```
## JavaScript `MIN_VALUE` and `MAX_VALUE`
`MAX_VALUE` returns the largest possible number in JavaScript
`MIN_VALUE` returns the lowest possible number in JavaScript

## Check if a number isPrime 

```js
let x = 5;
let isPrime = true;

for (let i = 2; i < x; i++>){
    if(x % i === 0){
        isPrime = false;
        break;
    }
}
```





