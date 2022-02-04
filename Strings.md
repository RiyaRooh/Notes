# JS Strings
### **JavaScript strings are for storing and manipulating text.**
*You can use quotes inside a string, as long as they don't match the quotes surrounding the string:*
```js
let answer1 = "It's alright";
let answer2 = "He is called 'Johnny'";
let answer3 = 'He is called "Johnny"';
```
### String Length
To find the ```length``` of a string, use the built-in length property:
```js
let text = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
let length = text.length; // => = 26
```
Because strings must be written within quotes, JavaScript will misunderstand this string:
```js
let text = "We are the so-called "Vikings" from the north.";
```
The string will be chopped to "We are the so-called ".

The solution to avoid this problem, is to use the backslash escape character.

The backslash ( `\` ) escape character turns special characters into string characters:
The sequence `\"`  inserts a double quote in a string:
```js
let text = "We are the so-called \"Vikings\" from the north.";
```
The sequence `\'`  inserts a single quote in a string:
```js
let text= 'It\'s alright.'; // => It's alright
```
## Extracting String Parts
    There are 3 methods for extracting a part of a string:
    - slice (start, end)
    - substring(start, end)
    - substr(start, length)

#### `slice()` extracts a part of a string and returns the extracted part in a new string.
The method takes 2 parameters: the start position, and the end position (end not included).

This example slices out a portion of a string from position 7 to position 12 (13-1):
```js
let str = "Apple, Banana, Kiwi";
let part = str.slice(7, 13); // => Banana
```
If you omit the second parameter, the method will slice out the rest of the string:
```js
let part = str.slice(7); // => Banana, Kiwi
```


