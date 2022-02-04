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

### `slice()` extracts a part of a string and returns the extracted part in a new string.
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
### JavaScript String `substring()`
`substring()` is similar to `slice()`

The difference is that `substring()` cannot accept negative indexes.
```js
let str = "Apple, Banana, Kiwi";
let part = str.substring(7, 13); // => Banana
```
If you omit the second parameter, `substring()` will slice out the rest of the string
### JavaScript String `substr()`
`substr()` is similar to `slice()`

The difference is that the second parameter specifies the length of the extracted part.
```js
let str = "Apple, Banana, Kiwi";
let part = str.substr(7, 6); // => Banana
```
If you omit the second parameter, `substr()` will slice out the rest of the string
### Replacing String Content
The `replace()` method replaces a specified value with another value in a string:
```js
let text = "Please visit Microsoft!";
let newText = text.replace("Microsoft", "W3Schools"); // => Please visit W3Schools!
```
**The `replace()` method does not change the string it is called on. The `replace()` method returns a new string**
By default, the `replace()` method replaces only the first match
To replace case insensitive, use a regular expression with an `/i` flag (insensitive):
```js
let text = "Please visit Microsoft!";
let newText = text.replace(/MICROSOFT/i, "W3Schools"); // => Please visit W3Schools!
```
To replace all matches, use a regular expression with a `/g` flag (global match):
```js
let text = "Please visit Microsoft and Microsoft!";
let newText = text.replace(/Microsoft/g, "W3Schools"); // => Please visit W3Schools and W3Schools!
```
### Converting to Upper and Lower Case
A string is converted to upper case with `toUpperCase()`

A string is converted to lower case with `toLowerCase()`
### JavaScript String `concat()`
`concat()` joins two or more strings:
```js
let text1 = "Hello";
let text2 = "World";
let text3 = text1.concat(" ", text2); // => Hello World!
```
The `concat()` method can be used instead of the `+` operator
## Extracting String Characters
There are 3 methods for extracting string characters:
- charAt(position)
- charCodeAt(position)
- Property access [ ]
### JavaScript String `charAt()`
The `charAt()` method returns the character at a specified index (position) in a string
```js
let text = "HELLO WORLD";
let char = text.charAt(0); // => H
```
### JavaScript String `charCodeAt()`
The `charCodeAt()` method returns the unicode of the character at a specified index in a string

[ASCII Table](https://www.asciitable.com/)
```js
let text = "HELLO WORLD";
let char = text.charCodeAt(0); // => 72 
```
### Property Access
```js
let text = "HELLO WORLD";
let char = text[0]; // => H
```
> Property access might be a little unpredictable: 
- It makes strings look like arrays (but they are not)
- If no character is found, [ ] returns undefined, while charAt() returns an empty string.
- It is read only. str[0] = "A" gives no error (but does not work!)

### JavaScript String `split()`
A string can be converted to an array with the `split()` method:
```js
text.split(",")    // Split on commas
text.split(" ")    // Split on spaces
text.split("|")    // Split on pipe
```
If the separator is "", the returned array will be an array of single characters:
```js
text.split("")
```
### JavaScript String `indexOf()`
The `indexOf()` method returns the index of (the position of) the first occurrence of a specified text in a string
```js
let str = "Please locate where 'locate' occurs!";
str.indexOf("locate"); // => 7
```
### JavaScript String `lastIndexOf()`
The `lastIndexOf()` method returns the index of the last occurrence of a specified text in a string:
```js
let str = "Please locate where 'locate' occurs!";
str.lastIndexOf("locate"); // =>21
```
> Both `indexOf()`, and `lastIndexOf()` return **-1** if the text is not found

Both methods accept a second parameter as the starting position for the search
```js
let str = "Please locate where 'locate' occurs!";
str.indexOf("locate", 15); // => 21
```
### JavaScript String `includes()`
The `includes()` method returns true if a string contains a specified value
```js
let text = "Hello world, welcome to the universe.";
text.includes("world"); // => true
```
### JavaScript String `startsWith()`
The `startsWith()` method returns true if a string begins with a specified value, otherwise false

**The `startsWith()` method is case sensitive.**
```js
let text = "Hello world, welcome to the universe.";

text.startsWith("Hello"); // => true
```
### JavaScript String `endsWith()`
The `endsWith()` method returns true if a string ends with a specified value, otherwise false

The `endsWith()` method is case sensitive


```js
var text = "John Doe";
text.endsWith("Doe"); // => true
```



