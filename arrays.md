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

#### filter()

#### find()

#### findIndex()

#### flat()

#### flatMap()

#### forEach()

#### from()

#### includes()

#### indexOf()

Returns the first position at which a given element appears in an array

```javascript
numbers.indexOf(3)
// 1
```

#### isArray()

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

#### of()

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

#### reduceRight()

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

#### toLocaleString()

#### toString()

#### unshift()

Adds one or more items to the start of the array and returns the new length

```javascript
fruit.unshift('Peach')                   
// ['Peach', 'Apple', 'Mango', 'Banana']
```

#### valueOf()

#### values()
