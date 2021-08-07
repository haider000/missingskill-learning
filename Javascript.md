<h1 align"center"> Javascript </h1>

* Javascript was the first scripting language that was supported natively by web
browsers, and thanks to this it gained a competitive advantage over any other
language and today it's still the only scripting language that we can use to
build Web Application
* JavaScript programming language was developed by Brendan Eich in 1995. 
* When JavaScript was created it was known as LiveScript. 
* Netscape changed its name to JavaScript. 
* JavaScript is a high-level, dynamic, lightweight, interpreted computer programming language. 
* It’s designed for creating network-centric apps. JavaScript is a dynamic type language, which means that you don't need to define type of the variable because it is effectively used by the JavaScript engine.
* ECMAScript is a standardized version of JavaScript with the goal of unifying the language's specifications and features. As all major browsers and JavaScript-runtimes follow this specification, the term ECMAScript is interchangeable with the term JavaScript.

## Javascript Data Types

JavaScript is a dynamic type language, which means that you don't need to define type of the variable because it is effectively used by the JavaScript engine. There are two types of data in JavaScript: primitive data type and non-primitive (reference) data type.


* **Primitive Datatypes** 
    1. Number 
    2. String
    3. Boolean 
    4. Undefined
    5. Symbol
    6. Null

* **Non-primitive Datatypes** 
    1. Object 
    2. Array
  

**Primitive Data Types**:
- Number - Stores integer and floating point numbers.  
```JavaScript
    var num=15;
```
- String - Stores text. In JavaScript, strings can’t be changed, and they must be inside of either double or single quotes.  
```JavaScript
    var firstName="Dipankar"; 
    var lastName='Chakraborty';
```
- Boolean - Stores true or false
```JavaScript
    var val=true;
```
- Null - Treated as falsy for boolean operations. In JavaScript null means nothing or empty. It’s something that doesn't exist. But in JavaScript, the data type of null is an object, which you can empty by setting an object to null.
```JavaScript
    var num=null;
```
- Undefined - A variable without a value is called undefined. It’s value and type are undefined, which means that the “value is not assigned”
```JavaScript
    var x;
```
 Symbol - new datatype introduced in ES6, a symbol value represents an unique identifier.
 
 **Non-Primitive Data Types**
 - Arrays - Stores several piece of data in one place
 ```JavaScript
    var sandwich = ["peanut butter", "jelly", "bread"]
 ```
 - Objects - It’s a collection of properties, which can reference any type of data, including objects and/or primitive values.
  ```JavaScript
      var cat = {
      "name": "Tom",
      "eyes": 2,
      "eyeColor": "brown"
      };
 ```
 

## Variables

A variable is a value assigned to an identifier, so you can reference and use it
later in the program.
This is because JavaScript is loosely typed, a concept you'll frequently hear
about.
A variable must be declared before you can use it.
We have 2 main ways to declare variables. 

# The first is to use const :

```const a = 0```

# The second way is to use let :

```let a = 0```

What's the difference?
const defines a constant reference to a value. This means the reference
cannot be changed. You cannot reassign a new value to it.
Using let you can assign a new value to it.
For example, you cannot do this:
```
const a = 0
a = 1
```

Because you'll get an error: TypeError: Assignment to constant variable. .
On the other hand, you can do it using let :
```
let a = 0
a = 1
14
```
const does not mean "constant" in the way some other languages like C
mean. In particular, it does not mean the value cannot change - it means it
cannot be reassigned. If the variable points to an object or an array (we'll see
more about objects and arrays later) the content of the object or the array can
freely change.
Const variables must be initialized at the declaration time:
```
const a = 0
```
but let values can be initialized later:
```
let a
a = 0
```

You can declare multiple variables at once in the same statement:
```
const a = 1, b = 2
let c = 1, d = 2
```
But you cannot redeclare the same variable more than one time:
```
let a = 1
let a = 2
```

Until 2015, var was the only way we could declare a variable in JavaScript.
Today, a modern codebase will most likely just use const and let .

# The third way of declaring a variable is using Var

```
var x = 10;
console.log(x);  //10

x = 20;
function fun() {
x = 30;                      //only functional scope
console.log("2", x);           //30
var x;                          //gets hoisted on top of the function
}
console.log("3", x);  //30
fun();
```

## Function

In JavaScript, we can divide up our code into reusable parts called functions.
```JavaScript
  function fun{
  console.log("Hello World");
  }
  fun();
```

In any moderately complex JavaScript program, everything happens inside
functions.
Functions are a core, essential part of JavaScript.
What is a function?
A function is a block of code, self contained.
Here's a function declaration:
```
function getData() {
// do something
}
```
A function can be run any times you want by invoking it, like this:
getData()
A function can have one or more argument:
```
function getData() {
//do something
}
function getData(color) {
//do something
}
function getData(color, age) {
//do something
}
```
When we can pass an argument, we invoke the function passing parameters:
```
function getData(color, age) {
//do something
}

getData('green', 24)
getData('black')
```
Note that in the second invokation I passed the black string parameter as
the color argument, but no age . In this case, age inside the function is
undefined .
We can check if a value is not undefined using this conditional:
```
function getData(color, age) {
//do something
if (typeof age !== 'undefined') {
//...
}
}
```
typeof is a unary operator that allows us to check the type of a variable.
You can also check in this way:
```
function getData(color, age) {
//do something
if (age) {
//...
}
}
```
although the conditional will also be true if age is null , 0 or an empty
string.
You can have default values for parameters, in case they are not passed:
```
function getData(color = 'black', age = 25) {
//do something
39
}
```
You can pass any value as a parameter: numbers, strings, booleans, arrays,
objects, and also functions.
A function has a return value. By default a function returns undefined , unless
you add a return keyword with a value:
```
function getData() {
// do something
return 'hi!'
}
```
We can assign this return value to a variable when we invoke the function:
```
function getData() {
// do something
return 'hi!'
}

let result = getData()
```
result now holds a string with the the hi! value.
You can only return one value.
To return multiple values, you can return an object, or an array, like this:
```
function getData() {
return ['Flavio', 37]
}
let [name, age] = getData()
Functions can be defined inside other functions:
const getData = () => {
const dosomething = () => {}
40
dosomething()
return 'test'
}
```
The nested function cannot be called from the outside of the enclosing
function.
You can return a function from a function, too.

## Scope Of Function

In JavaScript, scope refers to the visibility of variables. Variables which are defined outside of a function block have Global scope. This means, they can be seen everywhere in our JavaScript code.Variables which are defined within a function block have local scope.

```JavaScript
let name='bob'; //global scope
  function fun{
  let val='Hello' + name; //local scope
  console.log(val);
  }
  fun();
```

## Passing Primitive Parameter To Function

```JavaScript
function testFun(param1, param2) {
  console.log(param1, param2);
}
testFun(5,6);
```

## Passing Non-Primitive Parameter To Function
```Javascript
function fun(obj) {
  obj.make = 'Renault';
}
var car = {make: 'Fiat', model: 'Punto', year: 2018};
var x, y;
x = car.make; // x gets the value "Fiat"
fun(car);
y = car.make; // y gets the value "Renault"
```

## Function Returning A Function
```Javascript
function factorial(n) {
  if ((n === 0) || (n === 1))
    return 1;
  else
    return (n * factorial(n - 1));
```

## Function Passing As Parameter To Another Function

```Javascript
function map(f, a) {
  let result = []; // Create a new Array
  let i; // Declare variable
  for (i = 0; i <= a.length; i++)
    result[i] = f(a[i]);
  return result;
}
```

## Immediately Invoked Function Expression(IIFE)

Immediately Invoked Function Expression(IIFE) is a function that runs as soon as it is defined.
```JavaScript
(function () {
  let x;
  let y;
})();     // x and y will be discarded after the function is executed.
```

## Higher Order Function

A higher-order function can be defined as a function that accepts one or more functions as arguments and returns a function as a result.
```JavaScript
const numbers = [1, 2, 3, 4, 5];
const newArray = numbers.map((number) => number + 1);
console.log(numbers);
```

## Pure Function
Pure Function is a function that always returns the same result if the same arguments are passed.
```JavaScript
function calculateBankInterest( totalBalance ) {
    return totalBalance * 0.05;
}
```

## Arrow Function
Arrow functions allow us to write shorter function syntax. It was introduced in ES6. It doesn't get hoisted.
```JavaScript
let multiply = (a, b) => a * b;
console.log(multiply(7, 9));
```

## Objects
Objects are a collection of properties, which can reference any type of data, including objects and/or primitive values.
  ```JavaScript
      var smartphone = {
      "name": "Moto G40 Fusion",
      "cameras": 4,
      "color": "green"
      };
 ```
 
## Prototype Method Of Arrays

- **fill** - Fills the array with given value from start to end index
- **reverse** - Reverses the array
- **push** - Adds the given elements at end of the array
- **pop** - Removes last element from array
- **shift** - Removes first element from array
- **unshift** - Adds the given elements at start of the array
- **map** - Returns a new array of equal length that contains transformed elements
- **forEach** - Iterates an array and calls the given function

## Prototype Method Of String

- **toUpperCase** - Converts string to uppercase
- **toLowerCase** - Converts string to lowercase
- **split** - Divides the string into substrings
- **replace** - Replaces the existing string
- **toString** - Converts to string

## setTimeout And setInterval Function
setTimeout - allows us to run a function once after the interval of time.
setInterval - allows us to run a function repeatedly, starting after the interval of time, then repeating continuously at that interval.
```JavaScript
// repeat with the interval of 2 seconds
let timerId = setInterval(() => alert('tick'), 2000);
// after 5 seconds stop
setTimeout(() => { clearInterval(timerId); alert('stop'); }, 5000);
```
## JSON

JavaScript Object Notation (JSON) is a standard text-based format for representing structured data based on JavaScript object syntax. It is commonly used for transmitting data in web applications (e.g., sending some data from the server to the client, so it can be displayed on a web page, or vice versa).

```JavaScript
{
   "book": [
      {
         "id":"01",
         "language": "python",
         "edition": "9th",
         "author": "Traversy Media"
      },
      {
         "id":"02",
         "language": "Algorithms",
         "edition": "3rd",
         "author": "Coreman"
      }
   ]
}
```
The **JSON.stringify()** method converts a JavaScript object or value to a JSON string, optionally replacing values if a replacer function is specified or optionally including only the specified properties if a replacer array is specified.
```JavaScript
JSON.stringify(fun, ['week', 'month']);
```

## Spread Operator And Destructuring Feature Of ES6

**Spread Operator** allows an iterable such as an array expression or string to be expanded in places where zero or more arguments (for function calls) or elements (for array literals) are expected, or an object expression to be expanded in places where zero or more key-value pairs (for object literals) are expected.
```JavaScript
function myFunction(x, y, z) { }
let args = [0, 1, 2];
myFunction(...args);
```
ES6 provides a new feature called **destructing assignment** that allows you to destructure properties of an object or elements of an array into individual variables.
```JavaScript
function getPrices() {
   return [170, 380, 900];
}
let [x, y, z] = getPrices();
console.log(x); // 170
console.log(y); // 380
console.log(z); // 900
```
---
