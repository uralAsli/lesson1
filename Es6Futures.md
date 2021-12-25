
# ES6


|Sl.No|  Questions                                                     |
|----|-----------------------------------------------------------------|
| 01.|[Spread Operator](#Array.prototype.map())|
| 03.|[Rest Operator](#Array.prototype.reduce())|
| 04.|[Types](#Array.prototype.map())|


<br/>

## Q. Rest Operator
**Used to merge a list of function arguments into an array**
```javascript
function sortArgs(...args) {
    return args.sort()
}
```
## Examples:

**Used to split array elements or object properties**
```javascript
const number = 1;
const num2 = number;
const person = {
    name:'Asli'
}
const secondPerson = person;
person.name = 'ee';

// create purfectPerson :)
```

**Spread Operator**  
Spread operator allows iterables( arrays / objects / strings ) to be expanded into single arguments/elements.
Call sum function using spread operator
```javascript
function sum(x, y, z) {
  return x + y + z;
}

const numbers = [1, 2, 3];

```
**Copying an array**

```javascript
let fruits = ['Apple','Orange','Banana'];

```
**Concatenating arrays**  
```javascript
let arr1 = ['A', 'B', 'C'];

let arr2 = ['X', 'Y', 'Z'];

```
**Spreading elements together with an individual element **
Add new fruit to fruits array
```javascript
let fruits = ['Apple','Orange','Banana'];
```
**Spread syntax for object literals**
```javascript
let obj1 = { id: 101, name: 'Jhon Doe' }
let obj2 = { age: 25, country: 'USA'}
// Expected result: { "id": 101, "name": "Jhon Doe", "age": 25, "country": "USA" }

```
**Spreading elements on function calls**
```javascript
let fruits = ['Apple','Orange','Banana'];
// Expected result: Fruits: Apple, Orange and Banana
```
