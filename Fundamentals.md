# The Basics
## Code that is written inside a comment does not execute
How to create a comment:
- Normal comment ( shortcut ctrl + / )
  ```
  // comment // 
  ```
- Multi-line comment
```
    /*
    smth
    smth
    smth
    */
```
## Falsy Values
![image](https://i.ibb.co/PDNc9b6/Screenshot-2022-02-04-125120.png)
## Redeclaring Variables
Redeclaring a variable using the var keyword can impose problems. Redeclaring a variable inside a block will also redeclare the variable outside the block:
```js
var x = 10;
// Here x is 10

{
var x = 2;
// Here x is 2
}

// Here x is 2
```
sooooo you better use ```let```
```js
let x = 10;
// Here x is 10

{
let x = 2;
// Here x is 2
}

// Here x is 10
```
Redeclaring a variable with ```let```, in another block, IS allowed:
```js
let x = 2;    // Allowed

{
let x = 3;    // Allowed
}

{
let x = 4;    // Allowed
}
```
