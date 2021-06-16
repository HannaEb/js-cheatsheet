## Arrays

let fruit = ['Apple', 'Mango', 'Banana'];\
let veg = ['Carrot', 'Tomato', 'Pumpkin'];\
let numbers = [1, 3, 6, 4, 3, 2];\
let nums = [340, 91, 65, 5, 10];

### Methods

#### concat()

Joins several arrays into one

```javascript
fruit.concat(veg)                        
// ['Apple', 'Mango', 'Banana', 'Carrot', 'Tomato', 'Pumpkin']
```


#### copyWithin()

#### entries()

#### every()

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

#### flatMap()

#### forEach()

#### from()

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
