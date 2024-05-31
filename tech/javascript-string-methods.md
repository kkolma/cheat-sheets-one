Welcome to this comprehensive cheat sheet covering **38 JavaScript string methods**, categorized for easy reference. Whether you're a beginner or an experienced developer, you'll find clear explanations and examples to enhance your coding efficiency. For further reading and detailed documentation, visit the [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String). Happy coding!

## Creation Methods

### fromCharCode()
Creates a string from a sequence of Unicode values.
```javascript
console.log(String.fromCharCode(65, 66, 67)); // "ABC"
```

### fromCodePoint()
Creates a string from a sequence of code points.
```javascript
console.log(String.fromCodePoint(9731, 9733, 9734)); // "☃★☆"
```

### raw()
Creates a raw string from a template string.
```javascript
console.log(String.raw`Hello\nWorld`); // "Hello\nWorld"
```

## Accessor Methods

### String[@@iterator]()
Returns a new Iterator object that iterates over the code points of a string.
```javascript
const str = 'hello';
const iterator = str[Symbol.iterator]();
console.log(iterator.next().value); // "h"
```

### at()
Returns the character at the given index, allowing for positive and negative integers.
```javascript
const str = 'hello';
console.log(str.at(-1)); // "o"
```

### charAt()
Returns the character at the specified index.
```javascript
const str = 'hello';
console.log(str.charAt(1)); // "e"
```

### charCodeAt()
Returns the Unicode value of the character at the specified index.
```javascript
const str = 'hello';
console.log(str.charCodeAt(1)); // 101
```

### codePointAt()
Returns the code point value of the character at the specified index.
```javascript
const str = 'hello';
console.log(str.codePointAt(1)); // 101
```

## Transformation Methods

### concat()
Combines two or more strings.
```javascript
const str1 = 'Hello';
const str2 = 'World';
console.log(str1.concat(' ', str2)); // "Hello World"
```

### endsWith()
Checks if a string ends with a specified string/characters.
```javascript
const str = 'Hello world';
console.log(str.endsWith('world')); // true
console.log(str.endsWith('hello')); // false
```

### includes()
Checks if a string contains a specified string/characters.
```javascript
const str = 'Hello world';
console.log(str.includes('world')); // true
console.log(str.includes('hello')); // false
```

### indexOf()
Returns the index of the first occurrence of a specified value.
```javascript
const str = 'Hello world';
console.log(str.indexOf('o')); // 4
console.log(str.indexOf('z')); // -1
```

### isWellFormed()
Checks if a string is well-formed.
```javascript
const str = 'Hello world';
console.log(str.isWellFormed()); // true
```

### lastIndexOf()
Returns the index of the last occurrence of a specified value.
```javascript
const str = 'Hello world';
console.log(str.lastIndexOf('o')); // 7
console.log(str.lastIndexOf('z')); // -1
```

### localeCompare()
Compares two strings in the current locale.
```javascript
const str1 = 'a';
const str2 = 'b';
console.log(str1.localeCompare(str2)); // -1
```

### match()
Matches a string against a regular expression.
```javascript
const str = 'Hello world';
const regex = /world/;
console.log(str.match(regex)); // ["world"]
```

### matchAll()
Matches a string against a regular expression and returns an iterator.
```javascript
const str = 'Hello world';
const regex = /o/g;
for (const match of str.matchAll(regex)) {
  console.log(match);
}
// ["o"]
// ["o"]
```

### normalize()
Returns the Unicode Normalization Form of a string.
```javascript
const str = '\u1E9B\u0323';
console.log(str.normalize('NFC')); // "ẛ̣"
```

### padEnd()
Pads the current string with a specified string to a given length.
```javascript
const str = 'Hello';
console.log(str.padEnd(10, '!')); // "Hello!!!!!"
```

### padStart()
Pads the current string with a specified string to a given length.
```javascript
const str = 'Hello';
console.log(str.padStart(10, '!')); // "!!!!!Hello"
```

### repeat()
Returns a new string with a specified number of copies of the string.
```javascript
const str = 'Hello';
console.log(str.repeat(3)); // "HelloHelloHello"
```

### replace()
Replaces a specified value with another value in a string.
```javascript
const str = 'Hello world';
console.log(str.replace('world', 'there')); // "Hello there"
```

### replaceAll()
Replaces all occurrences of a specified value with another value in a string.
```javascript
const str = 'Hello world, world!';
console.log(str.replaceAll('world', 'there')); // "Hello there, there!"
```

### search()
Searches a string for a specified value and returns the position.
```javascript
const str = 'Hello world';
console.log(str.search('world')); // 6
```

### slice()
Extracts a part of a string and returns a new string.
```javascript
const str = 'Hello world';
console.log(str.slice(0, 5)); // "Hello"
```

### split()
Splits a string into an array of substrings.
```javascript
const str = 'Hello world';
console.log(str.split(' ')); // ["Hello", "world"]
```

### startsWith()
Checks if a string starts with a specified string/characters.
```javascript
const str = 'Hello world';
console.log(str.startsWith('Hello')); // true
console.log(str.startsWith('world')); // false
```

### substring()
Returns the part of the string between the start and end indexes.
```javascript
const str = 'Hello world';
console.log(str.substring(0, 5)); // "Hello"
```

### toLocaleLowerCase()
Converts a string to lowercase according to the host's locale.
```javascript
const str = 'HELLO WORLD';
console.log(str.toLocaleLowerCase()); // "hello world"
```

### toLocaleUpperCase()
Converts a string to uppercase according to the host's locale.
```javascript
const str = 'hello world';
console.log(str.toLocaleUpperCase()); // "HELLO WORLD"
```

### toLowerCase()
Converts a string to lowercase.
```javascript
const str = 'HELLO WORLD';
console.log(str.toLowerCase()); // "hello world"
```

### toString()
Returns a string representing the specified object.
```javascript
const str = 'Hello world';
console.log(str.toString()); // "Hello world"
```

### toUpperCase()
Converts a string to uppercase.
```javascript
const str = 'hello world';
console.log(str.toUpperCase()); // "HELLO WORLD"
```

### toWellFormed()
Ensures the string is well-formed.
```javascript
const str = 'Hello world';
console.log(str.toWellFormed()); // "Hello world"
```

### trim()
Removes whitespace from both ends of a string.
```javascript
const str = '  Hello world  ';
console.log(str.trim()); // "Hello world"
```

### trimEnd()
Removes whitespace from the end of a string.
```javascript
const str = '  Hello world  ';
console.log(str.trimEnd()); // "  Hello world"
```

### trimStart()
Removes whitespace from the beginning of a string.
```javascript
const str = '  Hello world  ';
console.log(str.trimStart()); // "Hello world  "
```

### valueOf()
Returns the primitive value of a string object.
```javascript
const str = new String('Hello world');
console.log(str.valueOf()); // "Hello world"
```
