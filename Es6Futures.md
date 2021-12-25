
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
**Find 1 in array**
```javascript
const arr = [1,2,3];
// Expected answer [1]
```

## Q. Primitive Types / Reference Types

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
