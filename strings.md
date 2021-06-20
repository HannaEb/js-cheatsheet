## Strings

let greeting = 'Hello world!';\
let food = 'fruit';\
let container = 'basket';\
let phrase = 'Luni and Marley are cute and naughty';\
let string = '     Good morning!      ';

### Methods 

#### charAt()

Returns the character at the specified index in a string 

```javascript 
greeting.charAt(1)
// e
```


#### charCodeAt()

Returns the Unicode of the character at the specified index or at index 0 if no index is specified

```javascript 
greeting.charCodeAt(3)
// 108
greeting.charCodeAt()
// 72
```


#### codePointAt()

Returns the UTF-16 code of the character at the specified index or at index 0 if no index is specified 

```javascript 
greeting.charCodeAt(3)
// 108
```

#### concat()

Joins two or more strings and returns the new string 

```javascript 
food.concat(' ', container)
// fruit basket
food.concat(container)
// fruitbasket
```


#### endsWith()

Determines whether the string ends with the specified characters and returns a boolean. The length of the string to be checked can be specified as a second argument

```javascript 
greeting.endsWith('world!')
// true
greeting.endsWith('world!', 10)
// false
greeting.endsWith('world!', 12)
// true
greeting.endsWith('World!')
// false
```


#### fromCharCode()

Converts Unicode numbers into characters

```javascript 
String.fromCharCode(72, 101, 108, 108, 111)
// Hello
```


#### fromCodePoint()

Returns a string created by using the specified sequence of code points 

```javascript 
String.fromCodePoint(72, 101, 108, 108, 111)
// Hello
```


#### includes()

Determines wheter the string contains the specified characters and returns a boolean

```javascript 
greeting.includes(' ')
// true
greeting.includes('llo')
// true
greeting.inlcudes('hello')
// false
```


#### indexOf()

Returns the position of the first occurrence of the specified value in the string, starting the search at a certain index. Returns -1 if the value is not found

```javascript 
phrase.indexOf('and')
// 5
phrase.indexOf('and', 10)
// 25
```


#### lastIndexOf()

Returns the position of the last occurrence of the specified value in the string, searching backwards. Returns -1 if the value is not found

```javascript 
phrase.lastIndexOf('and')
// 25
phrase.lastIndexOf('and', 10)
// 5
```


#### match()

Searches the string for a match against a regular expression and returns the matches as an Array object

```javascript 
phrase.match(/and/g)
// ['and', 'and']
phrase.match(/xyz/g)
// null
```


#### matchAll()

Returns an iterator of all results matching the regular expression

```javascript 
phrase.matchAll(/and/g)
// Object [RegExp String Iterator] {}
```


#### normalize()

Returns the Unicode Normalization Form of the string 

```javascript 
const hello = '\u0048\u0065\u006c\u006c\u006f'
console.log(hello)
// Hello
```


#### padEnd()

Pads the end of the current string with the specified characters so the resulting string reaches the specified length

```javascript 
food.padEnd(10, '.')
// fruit.....
```


#### padStart()

Pads the beginning of the current string with the specified characters so the resulting string reaches the specified length

```javascript 
food.padStart(10, '.')
// .....fruit
```


#### repeat()

Returns a new string with the original string copied the specified number of times

```javascript 
food.repeat(3)
// fruitfruitfruit
```


#### replace()

Returns a new string where the first occurrence of the specified value is replaced

```javascript 
phrase.replace('and', '&')
// Luni & Marley are cute and naughty
```


#### replaceAll()

Returns a new string where all occurrences of the specified value are replaced 

```javascript 
phrase.replaceAll('and', '&')
//Luni & Marley are cute & naughty
```


#### search() 

Searches the string for the specified value and returns the index of the match. Returns -1 if no match is found

```javascript 
phrase.search('and')
// 5
phrase.search(/and/g)
// 5
```


#### slice()

Extracts part of the string and returns it as a new string 

```javascript 
phrase.slice(9, 15)
// Marley
phrase.slice(-36, -32)
// Luni
phrase.slice(25)
// and naughty
```


#### split()

Splits the string into an array of substrings and returns the array

```javascript 
phrase.split()
// ['Luni and Marley are cute and naughty]
phrase.split(' ')
// ['Luni', 'and', 'Marley', 'are', 'cute', 'and', 'naughty']
```


#### startsWith()

Determines whether the string starts with the specified characters and returns a boolean

```javascript 
phrase.startsWith('Luni')
// true 
phrase.startsWith('Marley')
// false 
phrase.startsWith('Marley', 9)
// true
```


#### substring()

Extracts the characters between the two specified indices and returns the new string 

```javascript 
phrase.substring(0, 15)
// Luni and Marley
phrase.substring(20)
// cute and naughty
```


#### toLowerCase()

Converts the string to lowercase letters

```javascript 
phrase.toLowerCase()
// luni and marley are cute and naughty
```


#### toString()

Returns a string representing the specified object 

```javascript 
const array = ['Luni', 'Marley']
// Luni,Marley
```


#### toUpperCase()

Converts the string to uppercase letters 

```javascript
phrase.toUpperCase()
// LUNI AND MARLEY ARE CUTE AND NAUGHTY
```


#### trim()

Removes whitespace from both ends of a string 

```javascript 
string.trim()
// Good morning!
```


#### trimEnd()


#### trimStart()


#### valueOf()
