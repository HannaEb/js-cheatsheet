## Strings

let greeting = 'Hello world!';\
let food = 'fruit';\
let container = 'basket';\

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


#### lastIndexOf()


#### match()


#### matchAll()


#### normalize()


#### padEnd()


#### padStart()


#### raw()


#### repeat()


#### replace()


#### replaceAll()


#### search() 


#### slice()


#### split()


#### startsWith()


#### substring()


#### toLowerCase()


#### toString()


#### toUpperCase()


#### trim()


#### trimEnd()


#### trimStart()


#### valueOf()
