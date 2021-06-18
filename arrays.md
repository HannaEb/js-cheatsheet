## Arrays

let fruit = ['Apple', 'Mango', 'Banana'];\
let veg = ['Carrot', 'Tomato', 'Pumpkin'];\
let numbers = [1, 3, 6, 4, 3, 2];\
let nums = [340, 91, 65, 5, 10];\
let subs = [['Cat', 'Dog'], 'Bird', [[['Mouse']]]];

### Methods

#### concat()

Joins several arrays into one

```javascript
fruit.concat(veg)                        
// ['Apple', 'Mango', 'Banana', 'Carrot', 'Tomato', 'Pumpkin']
```


#### copyWithin()

Copies part of an array to another location in the same array and returns it without modifying its length

```javascript 
numbers.copyWithin(0, 4)
// [3, 2, 6, 4, 3, 2]
numbers.copyWithin()
// [4, 3, 6, 4, 3, 2]
numbers.copyWithin(1, 2, 5)
// [1, 6, 4, 3, 3, 2]
```


#### entries()

Returns an Array Iterator objext that contains the key/value pairs for each index in the array 

```javascript 
const keyvalues = fruit.entries()
for (const kv of keyvalues) {
  console.log(kv)
}
// [0, 'Apple']
// [1, 'Mango']
// [2, 'Banana']
```


#### every()

Tests whether all elements in the array pass a test provided by a function, retruns a boolean

```javascript 
fruit.every(f => typeof f === 'string')
// true
numbers.every(n => n > 5)
// false
```


#### fill()

Fills the specified elements in an array with a static value

```javascript
fruit.fill('Kiwi')
// ['Kiwi', 'Kiwi', 'Kiwi']
fruit.fill('Kiwi', 1, 3)
// ['Apple', 'Kiwi', 'Kiwi']
```


#### filter()

Creates a new array filled with all array elements that pass a test provided as a function

```javascript
numbers.filter(n => n > 2)
// [3, 6, 4, 3]
```


#### find()

Returns the value of the first element in an array that passes a test provided as a function

```javascript
numbers.find(n => n > 2)
// 3
```


#### findIndex()

Returns the index of the first element in an array that passes a test provided as a function

```javascript
numbers.findIndex(n => n === 6)
// 2
```


#### flat()

Creates a new array with all sub-arrays concatenated into it up to the specified depth

```javascript 
subs.flat()
// ['Cat', 'Dog', 'Bird', [['Mouse']]]
subs.flat(2)
// ['Cat', 'Dog', 'Bird', ['Mouse']]
subs.flat(Infinity)
// ['Cat', 'Dog', 'Bird', 'Mouse']
```


#### flatMap()

Returns a new array formed by applying the given function to each element of the array, and then flattening the result by one level

```javascript 
numbers.flatMap(n => [n * 2])
// [2, 6, 12, 8, 6, 4]
numbers.flatMap(n => [[n * 2]]
// [[2], [6], [12], [8], [6], [4]])
fruit.flatMap((f, index) => [f, index])
//['Apple', 0, 'Mango', 1, 'Banana', 2]
```


#### forEach()

Executes the provided function once for each element in the array, returns undefined 

```javascript 
fruit.forEach(f => console.log(f + 'pie'))
// 'Applepie'
// 'Mangopie'
// 'Bananapie'
```


#### from()

Creates a new array instance from an array-like or iterable object 

```javascript 
Array.from('cat')
// ['c', 'a', 't']
Array from([1, 2, 3], n => n + 2)
// [3, 4, 5]
```


#### includes()

Determines whether an array contains a specified element and returns a boolean

```javascript
  fruit.includes('Apple')
  // true
  fruit.includes('Melon')
  // false
  fruit.includes('Apple', 1)
  // false, search starts at index 1
  fruit.includes('banana')
  // false, the method is case sensitive
```


#### indexOf()

Returns the first position at which a given element appears in an array

```javascript
numbers.indexOf(3)
// 1
```


#### isArray()

Determines whether an object is an array and returns a boolean

```javascript
Array.isArray(fruit)
// true
```


#### join()

Combines all elements of an array into a single string

```javascript
fruit.join()
// 'Apple,Mango,Banana'
fruit.join(' ')
// 'Apple Mango Banana'
```


#### keys()

Returns an Array Iterator object with the keys of the array

```javascript 
const fruitkeys = fruit.keys()
for (const key of fruitkeys) {
  console.log(key)
}
// 0
// 1
// 3
```


#### lastIndexOf()

Returns the last position at which a given element appears in an array

```javascript
numbers.lastIndexOf(3)
// 4
```


#### map()

Creates a new array with the results of calling a function for every array element

```javascript
numbers.map(n => n * 2)
// [2, 6, 12, 8, 6, 4]
```


#### pop()

Removes the last element from the array and returns the element

```javascript
fruit.pop()
// returns 'Banana', fruit is now ['Apple, 'Mango']
```


#### push()

Adds one or more items to the end of the array and returns the new length

```javascript
fruit.push('Peach')                     
// ['Apple', 'Mango', 'Banana', 'Peach']
```


#### reduce()

Creates a new array with a single value by executing the provided function, starting from the beginning

```javascript
numbers.reduce((sum, n) => sum + n)
// 19
numbers.reduce((sum, n) => sum - n)
// -17
```


#### reduceRight()

Creates a new array with a single value by executing the provided function, starting from the end

```javascript
numbers.reduceRight((sum, n) => sum - n)
// -15
```


#### reverse()

Reverses the order of the items in the array

```javascript
fruit.reverse()
// ['Banana', 'Mango', 'Apple']
```


#### shift()

Removes the first element from the array and returns the element

```javascript
fruit.shift()
// returns 'Apple', fruit is now ['Mango', 'Banana']
```


#### slice()

Pulls a copy of a portion of an array into a new array. Does not change the original array

```javascript
numbers.slice(1, 3)
// [3, 6]
numbers.slice(-3, -1)
// [4, 3]
```


#### some()

Tests whether at least one lement in the array passes the test provided by the function, returns a boolean

```javascript 
numbers.some(n => n > 5)
// true
```


#### sort()

Sorts the elements in an array alphabetically or in ascending order for single digit numbers

```javascript
fruit.sort()
// ['Apple', 'Banana', 'Mango']
numbers.sort()
// [1, 2, 3, 3, 4, 6]
```

For numbers with more than two digits, we need to use a compare function

```javascript
nums.sort()
// [10, 340, 5, 65, 91]
nums.sort((a, b) => {return a - b})
// [5, 10, 65, 91, 340]
nums.sort((a, b) => {return b - a})
// [340, 91, 65, 10, 5]
```


#### splice()

Adds/removes items to/from an array and returns the removed items

```javascript
fruit.splice(1, 1, 'Kiwi')
// returns ['Mango'], fruit is now ['Apple', 'Kiwi', 'Banana']
fruit.splice(2, 0, 'Kiwi')
// returns [], fruit is now ['Apple', 'Mango', 'Kiwi', 'Banana']
fruit.splice(1, 2)
// returns ['Mango', 'Banana'], fruit is now ['Apple']
```


#### toString()

Returns a string with all the elements in the array, separated by commas

```javascript
fruit.toString()
// 'Apple,Mango,Banana'
```


#### unshift()

Adds one or more items to the start of the array and returns the new length

```javascript
fruit.unshift('Peach')                   
// ['Peach', 'Apple', 'Mango', 'Banana']
```


#### valueOf()

Returns the array itself

```javascript
fruit.valueOf()
// ['Apple', 'Mango', 'Banana']
```


#### values()

Returns an Array Iterator object that contains the values for each index in the array 

```javascript 
const fruitvalues = fruit.values()
for (const value of fruitvalues) {
  console.log(value)
}
// 'Apple'
// 'Mango'
// 'Banana'
```
