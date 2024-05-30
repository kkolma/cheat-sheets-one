Welcome to this comprehensive cheat sheet covering **43 JavaScript array methods**, categorized for easy reference. Whether you're a beginner or an experienced developer, you'll find clear explanations and examples to enhance your coding efficiency. For further reading and detailed documentation, visit the [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array). Happy coding!


## Creation Methods

### from()
Creates a new Array instance from an array-like or iterable object.
```javascript
const set = new Set(['foo', 'bar', 'baz']);
const array = Array.from(set);
console.log(array); // ["foo", "bar", "baz"]
```

### fromAsync()
Creates a new Array instance from an array-like or iterable object asynchronously.
```javascript
async function example() {
    const array = await Array.fromAsync(async function*() {
        yield 'foo';
        yield 'bar';
        yield 'baz';
    }());
    console.log(array); // ["foo", "bar", "baz"]
}
example();
```

### isArray()
Checks if the given value is an array.
```javascript
console.log(Array.isArray([1, 2, 3])); // true
console.log(Array.isArray('not an array')); // false
```

### of()
Creates a new Array instance with a variable number of arguments.
```javascript
const array = Array.of(1, 2, 3);
console.log(array); // [1, 2, 3]
```

## Accessor Methods

### Array[@@iterator]()
Returns a new Array Iterator object that contains the values for each index.
```javascript
const array = ['a', 'b', 'c'];
const iterator = array[Symbol.iterator]();
console.log(iterator.next().value); // "a"
```

### at()
Returns the element at the given index, allowing for positive and negative integers.
```javascript
const array = [1, 2, 3, 4];
console.log(array.at(-1)); // 4
```

### entries()
Returns a new Array Iterator object that contains the key/value pairs for each index.
```javascript
const array = ['a', 'b', 'c'];
const iterator = array.entries();
for (let entry of iterator) {
  console.log(entry);
}
// [0, "a"]
// [1, "b"]
// [2, "c"]
```

### includes()
Determines whether an array includes a certain value.
```javascript
const array = [1, 2, 3];
console.log(array.includes(2)); // true
console.log(array.includes(4)); // false
```

### indexOf()
Returns the first index at which a given element can be found.
```javascript
const array = [1, 2, 3, 1, 2, 3];
console.log(array.indexOf(2)); // 1
console.log(array.indexOf(4)); // -1
```

### join()
Joins all elements of an array into a string.
```javascript
const array = ['a', 'b', 'c'];
console.log(array.join('-')); // "a-b-c"
```

### keys()
Returns a new Array Iterator object that contains the keys for each index.
```javascript
const array = ['a', 'b', 'c'];
const iterator = array.keys();
for (let key of iterator) {
  console.log(key);
}
// 0
// 1
// 2
```

### lastIndexOf()
Returns the last index at which a given element can be found.
```javascript
const array = [1, 2, 3, 1, 2, 3];
console.log(array.lastIndexOf(2)); // 4
console.log(array.lastIndexOf(4)); // -1
```

### toString()
Returns a string representing the elements of the array.
```javascript
const array = [1, 2, 'a', 'b'];
console.log(array.toString()); // "1,2,a,b"
```

### toLocaleString()
Returns a localized string representing the elements of the array.
```javascript
const array = [1, 'a', new Date(Date.UTC(2021, 1, 1, 0, 0, 0))];
console.log(array.toLocaleString('en', { timeZone: 'UTC' }));
// "1,a,1/1/2021, 12:00:00 AM"
```

### values()
Returns a new Array Iterator object that contains the values for each index.
```javascript
const array = ['a', 'b', 'c'];
const iterator = array.values();
for (let value of iterator) {
  console.log(value);
}
// "a"
// "b"
// "c"
```

## Mutator Methods

### concat()
Merges two or more arrays into one new array.
```javascript
const array1 = [1, 2];
const array2 = [3, 4];
const newArray = array1.concat(array2);
console.log(newArray); // [1, 2, 3, 4]
```

### copyWithin()
Copies a part of the array to another location within the same array.
```javascript
const array = [1, 2, 3, 4, 5];
array.copyWithin(0, 3);
console.log(array); // [4, 5, 3, 4, 5]
```

### fill()
Fills all the elements of an array with a static value.
```javascript
const array = [1, 2, 3, 4];
array.fill(0, 2);
console.log(array); // [1, 2, 0, 0]
```

### pop()
Removes the last element from an array and returns that element.
```javascript
const array = [1, 2, 3];
const lastElement = array.pop();
console.log(lastElement); // 3
console.log(array); // [1, 2]
```

### push()
Adds one or more elements to the end of an array and returns the new length.
```javascript
const array = [1, 2];
const newLength = array.push(3, 4);
console.log(newLength); // 4
console.log(array); // [1, 2, 3, 4]
```

### reverse()
Reverses the order of the elements in an array.
```javascript
const array = [1, 2, 3];
array.reverse();
console.log(array); // [3, 2, 1]
```

### shift()
Removes the first element from an array and returns that element.
```javascript
const array = [1, 2, 3];
const firstElement = array.shift();
console.log(firstElement); // 1
console.log(array); // [2, 3]
```

### slice()
Returns a shallow copy of a portion of an array into a new array.
```javascript
const array = [1, 2, 3, 4];
const newArray = array.slice(1, 3);
console.log(newArray); // [2, 3]
```

### sort()
Sorts the elements of an array in place and returns the array.
```javascript
const array = [3, 1, 4, 1, 5];
array.sort();
console.log(array); // [1, 1, 3, 4, 5]
```

### splice()
Changes the contents of an array by removing or replacing existing elements and/or adding new elements.
```javascript
const array = [1, 2, 3, 4];
array.splice(1, 2, 'a', 'b');
console.log(array); // [1, "a", "b", 4]
```

### unshift()
Adds one or more elements to the beginning of an array and returns the new length.
```javascript
const array = [2, 3];
const newLength = array.unshift(1);
console.log(newLength); // 3
console.log(array); // [1, 2, 3]
```

### with()
Creates a new array with a modified value at the specified index.
```javascript
const array = [1, 2, 3];
const newArray = array.with(1, 'a');
console.log(newArray); // [1, "a", 3]
```

## Iteration Methods

### every()
Tests whether all elements in the array pass the provided function.
```javascript
const array = [1, 2, 3, 4];
const allBelowFive = array.every(num => num < 5);
console.log(allBelowFive); // true
```

### filter()
Creates a new array with all elements that pass the provided function.
```javascript
const array = [1, 2, 3, 4];
const filteredArray = array.filter(num => num > 2);
console.log(filteredArray); // [3, 4]
```

### find()
Returns the first element that passes the provided function.
```javascript
const array = [1, 2, 3, 4];
const foundElement = array.find(num => num > 2);
console.log(foundElement); // 3
```

### findIndex()
Returns the index of the first element that passes the provided function.
```javascript
const array = [1, 2, 3, 4];
const foundIndex = array.findIndex(num => num > 2);
console.log(foundIndex); // 2
```

### findLast()
Returns the last element that passes the provided function.
```javascript
const array = [1, 2, 3, 4];
const foundLastElement = array.findLast(num => num > 2);
console.log(foundLastElement); // 4
```

### findLastIndex()
Returns the index of the last element that passes the provided function.
```javascript


const array = [1, 2, 3, 4];
const foundLastIndex = array.findLastIndex(num => num > 2);
console.log(foundLastIndex); // 3
```

### flat()
Creates a new array with all sub-array elements concatenated into it.
```javascript
const array = [1, [2, 3], [4, [5]]];
const flatArray = array.flat(2);
console.log(flatArray); // [1, 2, 3, 4, 5]
```

### flatMap()
Maps each element using a mapping function, then flattens the result into a new array.
```javascript
const array = [1, 2, 3];
const flatMappedArray = array.flatMap(num => [num, num * 2]);
console.log(flatMappedArray); // [1, 2, 2, 4, 3, 6]
```

### forEach()
Executes a provided function once for each array element.
```javascript
const array = [1, 2, 3];
array.forEach(num => console.log(num * 2));
// 2
// 4
// 6
```

### map()
Creates a new array with the results of calling a provided function on every element.
```javascript
const array = [1, 2, 3];
const mappedArray = array.map(num => num * 2);
console.log(mappedArray); // [2, 4, 6]
```

### reduce()
Executes a reducer function on each element, resulting in a single output value.
```javascript
const array = [1, 2, 3, 4];
const sum = array.reduce((acc, num) => acc + num, 0);
console.log(sum); // 10
```

### reduceRight()
Executes a reducer function on each element from right to left, resulting in a single output value.
```javascript
const array = [1, 2, 3, 4];
const sum = array.reduceRight((acc, num) => acc + num, 0);
console.log(sum); // 10
```

### some()
Tests whether at least one element in the array passes the provided function.
```javascript
const array = [1, 2, 3, 4];
const hasEven = array.some(num => num % 2 === 0);
console.log(hasEven); // true
```

## Transformation Methods

### toReversed()
Returns a new array with the elements in reverse order.
```javascript
const array = [1, 2, 3];
const reversedArray = array.toReversed();
console.log(reversedArray); // [3, 2, 1]
```

### toSorted()
Returns a new array with the elements sorted.
```javascript
const array = [3, 1, 4, 1, 5];
const sortedArray = array.toSorted();
console.log(sortedArray); // [1, 1, 3, 4, 5]
```

### toSpliced()
Returns a new array with some elements removed/replaced and/or new elements added.
```javascript
const array = [1, 2, 3, 4];
const splicedArray = array.toSpliced(1, 2, 'a', 'b');
console.log(splicedArray); // [1, "a", "b", 4]
```
```
