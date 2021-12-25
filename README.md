# Long But Cool Questions 


|Sl.No|  Questions                                                     |
|----|-----------------------------------------------------------------|
| 01.|[Can you give an example for destructuring an object or an array?](#q-can-you-give-an-example-for-destructuring-an-object-or-an-array)|
| 02.|[List out important features of es6?](#q-list-out-important-features-of-es6)|
| 03.|[What is the benefit of using the arrow syntax for a method in a constructor?](#q-what-is-the-benefit-of-using-the-arrow-syntax-for-a-method-in-a-constructor)|
| 04.|[What are fat arrow functions? When you should not use arrow functions in ES6?](#q-what-are-fat-arrow-functions-when-you-should-not-use-arrow-functions-in-es6)|
| 06.|[How does await and async works in es6?](#q-how-does-await-and-async-works-in-es6)|
| 07.|[What are the benefits of using arrow function over es5 function?](#q-what-are-the-benefits-of-using-arrow-function-over-es5-function)|
| 08.|[What are the differences between ES6 class and ES5 function constructors?](#q-what-are-the-differences-between-es6-class-and-es5-function-constructors)|
| 09.|[What are the benefits of using spread syntax and how is it different from rest syntax?](#q-what-are-the-benefits-of-using-spread-syntax-and-how-is-it-different-from-rest-syntax)|
| 10.|[What are the differences between variables created using `let`, `var` or `const`?](#q-what-are-the-differences-between-variables-created-using-let-var-or-const)||
| 11.|[What is the difference between for..in and for..of?](#q-what-is-the-difference-between-forin-and-forof)|
| 12.|[What is the Temporal Dead Zone in ES6?](#q-what-is-the-temporal-dead-zone-in-es6)|
| 13.|[What is the difference between ES6 Map and WeakMap?](#q-what-is-the-difference-between-es6-map-and-weakmap)|
| 14.|[What are default values in destructuring assignment?](#q-what-are-default-values-in-destructuring-assignment)|
| 15.|[How do you swap variables using Destructuring Assignment?](#q-how-do-you-swap-variables-using-destructuring-assignment)|
| 16.|[What is the output of below spread operator array?](#q-what-is-the-output-of-below-spread-operator-array)|
| 17.|[What is modules in ES6?](#q-what-is-modules-in-es6)|
| 18.|[What is a trampoline function? What is it used for?](#q-what-is-a-trampoline-function-what-is-it-used-for)|
| 19.|[What is the difference between Set and WeakSet in ES6?](#q-what-is-the-difference-between-set-and-weakset-in-es6)|
| 20.|[What is difference between fetch() and XMLHttpRequest() in JavaScript?](#q-what-is-difference-between-fetch-and-xmlhttprequest-in-javascript)|
| 21.|[What is the difference between Promise and AJAX?](#q-what-is-the-difference-between-promise-and-ajax)|
| 22.|[What is use of Proxies in es6?](#q-what-is-use-of-proxies-in-es6)|
| 23.|[How could you make sure a const value is garbage collected?](#q-how-could-you-make-sure-a-const-value-is-garbage-collected)|

<br/>

## Q. Can you give an example for destructuring an object or an array?

Destructuring is an expression available in ES6 which enables a succinct and convenient way to extract values of Objects or Arrays and place them into distinct variables.

**Array Destructuring**

```javascript
// Variable assignment.
const foo = ['one', 'two', 'three'];
const [one, two, three] = foo;

console.log(one);
console.log(two);
console.log(three);
```

**Object Destructuring**

```javascript
// Variable assignment.
const object1 = { val1: 42, val2: true };
const { val1, val2} = object1;

console.log(val1);
console.log(val2);
```

<div align="right">
    <b><a href="#">↥ back to top</a></b>
</div>

## Q. List out important features of es6?

**1. Template Strings**  

Template literals are string literals allowing embedded expressions.
 
**Benefits**

* String interpolation
* Embedded expressions
* Multiline strings without hacks
* String formatting
* String tagging for safe HTML escaping, localization and more

```javascript
// String Substitution
let name = "Yeniyil";

// Multiline Strings

```

**2. Spread Operator**  
Spread operator allows iterables( arrays / objects / strings ) to be expanded into single arguments/elements.
Call sum function using spread operator
```javascript
function sum(x, y, z) {
  return x + y + z;
}

const numbers = [1, 2, 3];

```
**2.1. Copying an array**

```javascript
let fruits = ['Apple','Orange','Banana'];

```
**2.2. Concatenating arrays**  
```javascript
let arr1 = ['A', 'B', 'C'];

let arr2 = ['X', 'Y', 'Z'];

```
**2.3. Spreading elements together with an individual element **
Add new fruit to fruits array
```javascript
let fruits = ['Apple','Orange','Banana'];

**2.4. Spread syntax for object literals**
```javascript
let obj1 = { id: 101, name: 'Jhon Doe' }
let obj2 = { age: 25, country: 'USA'}

**3. Default Parametrs**

**4. Arrow Function (=>)**  
```javascript
var add = (x, y) => x + y;
```
**7. Arrow function with `this`**
```javascript
var person = {
  first: "Alex",
  actions: ["bike", "hike", "ski", "surf"],
  printActions: function() {
    var _this = this;
    this.actions.forEach(function(action) {
      var str = _this.first + " likes to " + action;
      console.log(str);
    });
  }
};
person.printActions();

//ES-6
var person = {
  first: "Alex",
  actions: ["bike", "hike", "ski", "surf"],
  printActions() {
    this.actions.forEach(action => {
      var str = this.first + " likes to " + action;
      console.log(str);
    });
  }
};
```

**8. Destructing Assignment**
```javascript
const person = {
  name: "Asli",
  gender: "Female",
};
 // print name of person


## Q. What is the benefit of using the arrow syntax for a method in a constructor?

The main advantage of using an arrow function as a method inside a constructor is that the value of `this` gets set at the time of the function creation and can't change after that. So, when the constructor is used to create a new object, `this` will always refer to that object. 
```javascript
const Person = function(firstName) {
  this.firstName = firstName;
  this.sayName1 = function() { console.log(this.firstName); };
  this.sayName2 = () => { console.log(this.firstName); };
};

```
The main takeaway here is that `this` can be changed for a normal function, but the context always stays the same for an arrow function. So even if you are passing around your arrow function to different parts of your application, you wouldn\'t have to worry about the context changing.

<div align="right">
    <b><a href="#">↥ back to top</a></b>
</div>

## Q. What are fat arrow functions? When you should not use arrow functions in ES6?

An arrow function is a shorter syntax for a function expression and does not have its own **this, arguments, super, or new.target**. These function are best suited for non-method functions, and they cannot be used as constructors.


**Arrow functions in ES6 has two limitations**:
* Don't work with new
* Fixed this bound to scope at initialisation

**When should not use Arrow Functions**  
**1. Object methods**  
When you call cat.jumps, the number of lives does not decrease. It is because this is not bound to anything, and will inherit the value of this from its parent scope.
```javascript
var cat = {
  lives: 9,
  jumps: () => {
    this.lives--;
  }
}
```
**2. Callback functions with dynamic context**  
If we click the button, we would get a TypeError. It is because this is not bound to the button, but instead bound to its parent scope.
```javascript
var button = document.getElementById('press');
button.addEventListener('click', () => {
  this.classList.toggle('on');
});
```
<div align="right">
    <b><a href="#">↥ back to top</a></b>
</div>


## Q. What are the benefits of using spread syntax and how is it different from rest syntax?

ES6's spread syntax is very useful when coding in a functional paradigm as we can easily create copies of arrays or objects without resorting to `Object.create`, `slice`, or a library function. This language feature is used often in Redux and Rx.js projects.

```javascript
function addCookiesInArray(arr) {
  return [...arr, 'Cookies'];
}

const result = addCookiesInArray(['I', 'really', "don't", 'like']); 

console.log(result); // ["I", "really", "don't", "like", "Cookies"]
```

```javascript
const person = {
  name: 'Todd',
  age: 29,
};

const copyOfPerson = { ...person };

console.log(copyOfPerson); // {name: "Todd", age: 29}
```

ES6's rest syntax offers a shorthand for including an arbitrary number of arguments to be passed to a function. It is like an inverse of the spread syntax, taking data and stuffing it into an array rather than unpacking an array of data, and it works in function arguments, as well as in array and object destructuring assignments.

```javascript
function addFiveToABunchOfNumbers(...numbers) {
  return numbers.map(x => x + 5);
}

const result = addFiveToABunchOfNumbers(4, 5, 6, 7, 8, 9, 10); // [9, 10, 11, 12, 13, 14, 15]

const [a, b, ...rest] = [1, 2, 3, 4]; // a: 1, b: 2, rest: [3, 4]

const { e, f, ...others } = {
  e: 1,
  f: 2,
  g: 3,
  h: 4,
}; // e: 1, f: 2, others: { g: 3, h: 4 }
```
<div align="right">
    <b><a href="#">↥ back to top</a></b>
</div>

## Q. What are the differences between variables created using `let`, `var` or `const`?

Variables declared using the `var` keyword are scoped to the function in which they are created, or if created outside of any function, to the global object. `let` and `const` are _block scoped_, meaning they are only accessible within the nearest set of curly braces (function, if-else block, or for-loop).

```javascript
function foo() {
  // All variables are accessible within functions.
  var bar = 'bar';
  let baz = 'baz';
  const qux = 'qux';

  console.log(bar); // bar
  console.log(baz); // baz
  console.log(qux); // qux
}

console.log(bar); // ReferenceError: bar is not defined
console.log(baz); // ReferenceError: baz is not defined
console.log(qux); // ReferenceError: qux is not defined
```

```javascript
if (true) {
  var bar = 'bar';
  let baz = 'baz';
  const qux = 'qux';
}

// var declared variables are accessible anywhere in the function scope.
console.log(bar); // bar
// let and const defined variables are not accessible outside of the block they were defined in.
console.log(baz); // ReferenceError: baz is not defined
console.log(qux); // ReferenceError: qux is not defined
```

`var` allows variables to be hoisted, meaning they can be referenced in code before they are declared. `let` and `const` will not allow this, instead throwing an error.

```javascript
console.log(foo); // undefined

var foo = 'foo';
console.log(baz); // ReferenceError: can't access lexical declaration 'baz' before initialization

let baz = 'baz';
console.log(bar); // ReferenceError: can't access lexical declaration 'bar' before initialization

const bar = 'bar';
```

Redeclaring a variable with `var` will not throw an error, but 'let' and 'const' will.

```javascript
var foo = 'foo';
var foo = 'bar';
console.log(foo); // "bar"

let baz = 'baz';
let baz = 'qux'; // Uncaught SyntaxError: Identifier 'baz' has already been declared
```

`let` and `const` differ in that `let` allows reassigning the variable's value while `const` does not.

```javascript
// This is fine.
let foo = 'foo';
foo = 'bar';

// This causes an exception.
const baz = 'baz';
baz = 'qux';
```
<div align="right">
    <b><a href="#">↥ back to top</a></b>
</div>

## Q. What is the difference between for..in and for..of?
* **for in**: loops over enumerable property names of an object.
* **for of**: (new in ES6) does use an object-specific iterator and loops over the values generated by that.

Both `for..of` and `for..in` statements iterate over lists; the values iterated on are different though, `for..in` returns a **list of keys** on the object being iterated, whereas `for..of` returns a **list of values** of the numeric properties of the object being iterated.  
Example:
```javascript
let list = [4, 5, 6];

for (let i in list) {
   console.log(i); // "0", "1", "2",
}

for (let i of list) {
   console.log(i); // "4", "5", "6"
}
```
<div align="right">
    <b><a href="#">↥ back to top</a></b>
</div>


## Q. What are default values in destructuring assignment?

A variable can be assigned a default value when the value unpacked from the array or object is undefined during destructuring assignment. It helps to avoid setting default values separately for each assignment.  

**Array Destructuring**  
```javascript
var x, y, z;

[x=2, y=4, z=6] = [10];
console.log(x); // 10
console.log(y); // 4
console.log(z); // 6
```

**Object Destructuring**  
```javascript
var {x=2, y=4, z=6} = {x: 10};

console.log(x); // 10
console.log(y); // 4
console.log(z); // 6
```
## Q. How do you swap variables using Destructuring Assignment?
```javascript
var x = 10, y = 20;

[x, y] = [y, x];
console.log(x); // 20
console.log(y); // 10
```
## Q. What is the output of below spread operator array?
```javascript
[...'John']
```
**Output**:  ['J', 'o', 'h', 'n']  
**Explanation**: The string is an iterable type and the spread operator with in an array maps every character of an iterable to one element. Hence, each character of a string becomes an element within an Array.

<div align="right">
    <b><a href="#">↥ back to top</a></b>
</div>

**Exporting**
```javascript
export const myNumbers = [1, 2, 3, 4];
const animals = ['Panda', 'Bear', 'Eagle']; // Not available directly outside the module

export function myLogger() {
  console.log(myNumbers, animals);
}

export class Alligator {
   constructor() {
     // ...
   }
}
```

**Default export**
```javascript
export const myNumbers = [1, 2, 3, 4];
const animals = ['Panda', 'Bear', 'Eagle'];

export default function myLogger() {
  console.log(myNumbers, pets);
}

export class Alligator {
  constructor() {
    // ...
  }
}
```

<div align="right">
    <b><a href="#">↥ back to top</a></b>
</div>

## Q. What is a trampoline function? What is it used for? 

The trampoline is just a technique to optimize **recursion** and prevent `stack-overflow` exceptions in languages that don't support tail call optimization like Javascript ES5 implementation. However, ES6 will probably have support for tail call optimization.

The problem with regular recursion is that every recursive call adds a stack frame to the call stack, which you can visualize as a **pyramid** of calls. Here is a visualization of calling a factorial function recursively:
```
(factorial 3)
(* 3 (factorial 2))
(* 3 (* 2 (factorial 1)))
(* 3 (* 2 (* 1 (factorial 0)))) 
(* 3 (* 2 (* 1 1)))
(* 3 (* 2 1))
(* 3 2)
6
```
Here is a visualization of the stack where each vertical dash is a stack frame:
```
         ---|---
      ---|     |---
   ---|            |--- 
---                    ---
```
The problem is that the stack has limited size, and stacking up these stack frames can overflow the stack. Depending on the stack size, a calculation of a larger factorial would overflow the stack. That is why regular recursion in Javascript could be considered dangerous.

An optimal execution model would be something like a **trampoline** instead of a **pyramid**, where each recursive call is executed in place, and does not stack up on the call stack. That execution in languages supporting tail call optimization could look like:
```
(fact 3)
(fact-tail 3 1)
(fact-tail 2 3)
(fact-tail 1 6)
(fact-tail 0 6)
6
```
You can visualize the stack like a bouncing trampoline:
```
   ---|---   ---|---   ---|---
---      ---       ---       
```
This is clearly better since the stack has always only one frame, and from the visualization you can also see why it is called a trampoline. This prevents the stack from overflowing.

Since we don't have the luxury of `tail call optimization` in Javascript, we need to figure out a way to turn regular recursion into an optimized version that will execute in trampoline-fashion.

One obvious way is to **get rid of recursion**, and rewrite the code to be iterative.

When that is not possible we need a bit more complex code where instead of executing directly the recursive steps, we will utilize `higher order functions` to return a wrapper function instead of executing the recursive step directly, and let another function control the execution.

In your example, the **repeat** function wraps the regular recursive call with a function, and it returns that function instead of executing the recursive call:
```javascript
function repeat(operation, num) {
    return function() {
       if (num <= 0) return
       operation()
       return repeat(operation, --num)
    }
}
```
The returned function is the next step of recursive execution and the trampoline is a mechanism to execute these steps in a controlled and iterative fashion in the while loop:
```javascript
function trampoline(fn) {
    while(fn && typeof fn === 'function') {
        fn = fn()
    }
}
```
So the sole purpose of the trampoline function is to control the execution in an iterative way, and that ensures the stack to have only a single stack frame on the stack at any given time.

Using a trampoline is obviously less performant than simple recursion, since you are "blocking" the normal recursive flow, but it is much safer.


<div align="right">
    <b><a href="#">↥ back to top</a></b>
</div>
