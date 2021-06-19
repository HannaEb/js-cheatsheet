## Loops

### For Loop 

Executes a block of code a given number of times

```javascript 
for (let i = 0; i < 3; i++) {
    console.log('Number ' + i);
}
// Number 0 
// Number 1
// Number 2
```


### For In Loop 

Loops through the properties of an object, each iteration returns a key 

```javascript 
const numbers = [4, 5, 6]
for (let i in numbers) {
    console.log('Number ' + i);
}
// Number 0
// Number 1
// Number 2
```


### For Of Loop

Loops through the values of iterable objects such as arrays, strings, maps etc

```javascript 
const numbers = [4, 5, 6]
for (let i of numbers) {
    console.log('Number ' + i);
}
// Number 4
// Number 5
// Number 6
```


### While Loop 

Executes a block of code as long as the specified condition is true

```javascript 
let i = 0;
while (i < 3) {
    console.log('Number ' + i);
    i++;
}
// Number 0 
// Number 1 
// Number 2
```


### Do While Loop

Executes a block of code until the specified condition evaluates to false. As the condition is evaluated after the statement, it executes at least once

```javascript 
let i = 0;
do {
    console.log('Number ' + i);
    i++;
} while (i < 3);
// Number 0 
// Number 1 
// Number 2
do {
    console.log('Number ' + i);
    i++
} while i > 3;
// Number 0
```


### Break

Terminates the current loop 

```javascript 
let i = 0;
while (i < 10) {
    if (i === 3) {
        break;
    }
    console.log('Number ' + i);
}
// Number 0 
// Number 1
// Number 2
for (i = 0; i < 10; i++) {
    if (i ===3) {
        break;
    }
    console.log('Number ' + i);
}
// Number 0
// Number 1
// Number 2
```


### Continue

Breaks one iteration if a specified condition evaluates to true and continues with the next iteration in the loop

```javascript 
for (let i = 0; i < 5; i++) {
    if (i === 3) {
        continue;
    }
    console.log('Number ' + i);
}
// Number 0 
// Number 1
// Number 2
// Number 4
```
