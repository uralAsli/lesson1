# Long But Cool Questions 


|Sl.No|  Questions                                                     |
|----|-----------------------------------------------------------------|
| 01.|[map example](#Array.prototype.map())|
| 02.|[filter example](#Array.prototype.filter())|
| 03.|[reduce example](#Array.prototype.reduce())|

<br/>

## Q. Array.prototype.map()

[Map Doc](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)

**Calling functions on each item in an array**
```javascript
// Multiply each element in the array by 3 using map 
const numberArr = [1, 2, 3];
// expected answer = [1, 6, 9];
```
**Coverting a String to an Array**
```javascript
// Variable assignment.
const name = "PATATES";
// expected answer = ["P", "A", "T", "A", "T", "E", "S"];
```
**Rendering Lists**

[codesandbox](https://codesandbox.io/s/example-of-map-w1gw8?file=/src/index.js)
```javascript
const names = ["yasasin", "yeni", "yil"];
```
**Reformatting Array Object**
```javascript
// Calculate users' age by the lengths of their favorite food times 10
const myUsers = [
    { name: 'asli', likes: 'patates' },
    { name: 'ural', likes: 'hamsi' }
];
// expected answer = [{age: 40, asli: "patates"}, {age: 40, ural: "hamsi"}];
```

<div align="right">
    <b><a href="#">↥ back to top</a></b>
</div>

## Q. Array.prototype.filter()

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

## Q. Array.prototype.reduce()

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
