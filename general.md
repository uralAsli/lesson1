# Long But Cool Questions 

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
**2. Default Parametrs**

**3. Arrow Function (=>)**  
```javascript
var add = (x, y) => x + y;
```
**7. Arrow function with `this`**

Arrow functions do not bind their own this, instead, they inherit the one from the parent scope, which is called "lexical scoping". This makes arrow functions to be a great choice in some scenarios but a very bad one in others

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

## Q. What are the differences between variables created using `let`, `var` or `const`?

Variables declared using the `var` keyword are scoped to the function in which they are created, or if created outside of any function, to the global object. `let` and `const` are _block scoped_, meaning they are only accessible within the nearest set of curly braces (function, if-else block, or for-loop).

```javascript
function foo() {
  // All variables are accessible within functions.
  var bar = 'bar';
  let baz = 'baz';
  const qux = 'qux';

  console.log(bar);
  console.log(baz);
  console.log(qux);
}

console.log(bar);
console.log(baz);
console.log(qux);
```

```javascript
if (true) {
  var bar = 'bar';
  let baz = 'baz';
  const qux = 'qux';
}

console.log(bar);
console.log(baz);
console.log(qux);
```

`var` allows variables to be hoisted, meaning they can be referenced in code before they are declared. `let` and `const` will not allow this, instead throwing an error.

```javascript
console.log(foo);

var foo = 'foo';
console.log(baz);

let baz = 'baz';
console.log(bar);

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
