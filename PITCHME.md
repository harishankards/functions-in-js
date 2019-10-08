# Functions in Javascript
____

What you really need to know! 

---
## What is a function?

A function is a body of code that: 
- Might receive some data called parameters,
- Use the data for its job, 
- And might return something when it’s done.

```
function name(parameter1, parameter2, parameter3) {
  // code to be executed
}

```
---
## How do you call a function?

- Functions are used by just calling their names. 
- Functions can be called as many times as needed...or as you want

---
## Need an example? 🤓

Here you go:

```
function sendMoney(accountNumber, amount) {
    findAccount(accountNumber).balance += amount;
    return myAccount.balance; 
}
```

Calling it!

```
while(true) {
 sendMoney(‘0423679273’, 5000); 
}
```
---

## Ways to declare functions in JavaScript!

- Majorly, we have two ways to describe functions in JS.

- There are over 5 ways functions can be declared in JavaScript.

    1. Function declaration
    2. Function expression
    3. Shorthand method definition
    4. Arrow functions
    5. Generator functions

---
## 1. Function declaration

```
function greet(name){
 console.log(`Hi ${name}`);
}

function sum(a, b) {
 return a + b;
}
```
---
## 2. Function expression

- A function expression is that which is assigned to a variable.
- You can add an optional name after the “function”. But it won't be having any effect.

```
const greet = function(name){
 console.log(`Hi ${name}`);
}

const sum = function plus(a, b) {
 return a + b;
}
```

---
## 3. Shorthand method definition

- This is used in object literals and ECMAScript 6 to define functions.
- They do not use the `function` keyword.

```
class Star {
    constructor(name) {
        this.name = name;
    }
    getMessage(message) {
        return this.name + message;
    } 
}

const sun = new Star('Sun');
sun.getMessage(' is shining')
// => 'Sun is shining'
```
---
## 4. Arrow functions
- Arrow functions are defined by parenthesis `()` containing the parameters, followed by the arrow `=>` and then the body of the function enclosed by `{` and `}`.

```
const greet = (name) => {
    console.log(`Hi ${name}`);
}

const sum = (a, b) => {
    return a + b;
}
```
---
## 5. Generator functions
#### You can ignore me 🤓
- Generator functions are like normal functions but they don’t use return, they `yield`, although they return a Generator object.
- A generator function starts with `function*` and uses yield instead of return

```
function* indexGenerator(){
    var index = 0;
    while(true) {
        yield index++;
    }
}

const g = indexGenerator();
console.log(g.next().value); // => 0
console.log(g.next().value); // => 1
```
---
## Callback functions
- A callback function is a function passed as a parameter to another function call. In the called function, the callback function is called; most times after it is done with its process.
- This aids the asynchronous feature of Js

```
// add() function is called with arguments a, b 
// and callback, callback will be executed just  
// after ending of add() function 
function add(a, b , callback){ 
   document.write(`The sum of ${a} and ${b} is ${a+b}.` +"<br>"); 
   callback(); 
} 
     
// disp() function is called just 
// after the ending of add() function  
function disp(){ 
   document.write('This must be printed after addition'); 
} 
     
// Calling add() function 
add(5,6,disp);
```

**NOTE**: Keep callbacks to a minimal in order to avoid callback hell.😵

---
## Callback HELL

A callback hell is basically when you have lot of cascaded callbacks that it starts to not make sense and drive you nuts!