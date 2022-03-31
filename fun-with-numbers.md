#  Math Methods

## Math.round()
>- `Math.round(x)` returns the nearest integer
## Math.ceil()
>- `Math.ceil(x)` returns the value of x rounded **up** to its nearest integer
## Math.floor()
>- `Math.floor(x)` returns the value of x rounded **down** to its nearest integer
## Math.trunc()
>- `Math.trunc(x)` returns the integer part of x
```js
Math.trunc(4.9); // => 4
```
## Math.pow()
>- `Math.pow(x, y)` returns the value of x to the power of y
## Math.sqrt()
>- `Math.sqrt(x)` returns the square root of x
## Math.min() and Math.max()
>- `Math.min()` and `Math.max()` can be used to find the lowest or highest value in a list of arguments

## Math.abs()
>- `The Math.abs()` function returns the absolute value of a number. That is, it returns x if x is positive or zero, and the negation of x if x is negative.

```
function difference(a, b) {
  return Math.abs(a - b);
}

console.log(difference(3, 5));
// expected output: 2

console.log(difference(5, 3));
// expected output: 2

console.log(difference(1.23456, 7.89012));
// expected output: 6.6555599999999995
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

let number = +gets();

function(isPrimeNumber(n)){
    for (var = 2; i < n; i++>){
        if(n % 2 === 0) return false;
    }
    return true;
}
```

## Get the second number only in an equation
```js
8 + 8 = 16
(8 + 8) % 10 = 6
```

