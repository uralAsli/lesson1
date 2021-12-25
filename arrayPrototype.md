# Long But Cool Questions 


|Sl.No|  Questions                                                     |
|----|-----------------------------------------------------------------|
| 01.|[map example](#Array.prototype.map())|
| 02.|[filter example](#Array.prototype.filter())|
| 03.|[reduce example](#Array.prototype.reduce())|

<br/>

## Q. Array.prototype.map()

[Map Doc](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)

**Summing an Array using reduce**
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

**Basic filter**  
```javascript
//Numbers greater than 7
let numbers = [1, 3, 6, 8, 11];
// expected answer = [8,11];
```
**Basic filter**  
```javascript
// filter funny character
const creatures = [
    {name: "SpongeBob", personality: "Funny"},
    {name: "Mater", personality: "Funny"},
    {name: "Gargamel", personality: "Antagonistic"},
    {name: "Voldemort", habitat: "Unkind"}
];
// expected answer  = [ {name: "SpongeBob", personality: "Funny"}, {name: "Mater", personality: "Funny"}];
```

## Q. Array.prototype.reduce()

**Summing each value in array**:

![alt text](https://miro.medium.com/max/1210/1*4PlcDrCnIIGHL-bEQk0qmQ.png)

```javascript

let data = [2, 4, 6, 8];
// expected answer = 20;
```
**Counting Occurrences of Items in an Array**  
```javascript
// filter funny character
const fruits = [ 'Banana', 'Dragon', 'Apple', 'Orange', 'Pear', 'Elderberry']
// expected answer 10
```

**Getting Max Length in Array**  
```javascript
// getting max-length || min-length value from an array using reduce
const fruits = [ 'Banana', 'Dragon', 'Apple', 'Orange', 'Pear', 'Elderberry']
console.log(max); // 10
```
