This comprehensive JSON Cheat Sheet is your go-to resource for mastering JSON, the lightweight, text-based data interchange format. From syntax basics, types, and examples to parsing and stringification in JavaScript, it covers essential aspects to enhance your data handling skills. Whether you're learning JSON for the first time or brushing up on specifics like encoding, security, and performance considerations, this cheat sheet offers succinct, actionable information to streamline your development process.

## Getting Started
### Introduction

[JSON](https://json.org/) is a lightweight text-based open standard designed for human-readable data interchange.

- JSON stands for JavaScript Object Notation
- JSON is easy to read and write.
- JSON is language agnostic data-interchange format
- JSON filename extension is `.json`
- JSON Internet Media type is `application/json`



### Examples

```json
{
  "name": "Jason",
  "age": 39,
  "height": 1.92,
  "gender": "M",
  "salary": 70000,
  "married": true,
  "children": [
    {"name": "Tom", "age": 9, "gender":"M"},
    {"name": "Ava", "age": 7, "gender":"F"}
  ]
}
```

### Comments in JSON

Standard JSON does not support comments.
#### Workarounds:
- **Use external documentation**: Document the JSON structure separately.
- **Non-standard solutions**: Some developers use `_comment` keys for comments, but this is not officially supported and can be ignored by parsers.

#### Note:
- For development purposes, some tools support JSON with comments (JSONC), but always convert to standard JSON for production to ensure compatibility.


### JSON Encoding

JSON is typically encoded in UTF-8.

#### Key Points:
- **UTF-8 Encoding**: Ensures compatibility across different platforms and supports international character sets.
- **Ensure encoding consistency** across the creation, storage, and parsing phases to avoid errors.


### Types

| Type      | Description                             |
|-----------|-----------------------------------------|
| [`String`](#string)  | Series of characters                    |
| [`Number`](#number)  | Double precision floating-point         |
|  [`Boolean`](#boolean) | `true` or `false`                       |
| [`Array`](#arrays)   | Ordered sequence of values              |
| [`Object`](#objects)  | Unordered collection of key/value pairs |
| [`null`](#null)    | Null or Empty                           |




### String
|      |                            |
|------|----------------------------|
| `"` | Double quote               |
| `\` | Backslash                  |
| `/` | Forward slash              |
| `\b` | Backspace                  |
| `\f` | Form feed                  |
| `\n` | Newline                    |
| `\r` | Carriage return            |
| `\t` | Tab                        |
| `\u` | Trailed by four hex digits |

#### Examples
```json
{
  "url": "https://cheatsheets.one",
  "msg" : "Hi,\n\"CheatSheets.one\"",
  "intro": "Share cheat sheet and quick reference for anyone."
}
```
#### Invalid String
```json
{ "foo": 'bar' }
```
Have to be delimited by double quotes



### Number

| Type       | Description                            |
|------------|----------------------------------------|
| `Integer`  | Digits 1-9, 0 and positive or negative |
| `Fraction` | Fractions like 0.3, 3.9                |
| `Exponent` | Exponent like e, e+, e-, E, E+, E      |

#### Examples
```json
{
  "positive" : 12,
  "negative" : -1,
  "fraction" : 10.25,
  "exponent" : 1.0E+2,
  "zero" : 0
}
```
#### Invalid Number
```json
{ "foo": 0xFF }
```
In JSON you can use only Decimal Literals


### Boolean

In JSON, Booleans are represented by two literal values:

- `true`
- `false`

#### Examples:

```json
{
  "isActive": true,
  "isVerified": false
}
```

### Objects

```json
{
  "color": "Purple",
  "id": "210",
  "composition": {
    "R": 70,
    "G": 39,
    "B": 89
  },
  "empty_object": {}
}
```

Multiple key/value pairs separated by a comma



### Arrays
```json
[1, 2, 3, 4, 5]
```
Begins with `[` and ends with `]`



### Array of objects
```json
{
  "children": [
    {"name": "Jimmy Smith", "age": 15},
    {"name": "Sammy Sosa", "age": 12}
  ]
}
```


### Object of arrays
```json
{
  "attributes": ["a1", "a2"],
  "methods": ["getter", "setter"],
  "empty_array": []
}
```


### 2D Array
```json
{
  "my_sequences": [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9, 0],
    [10, 11]
  ]
}
```


### Object of objects

```json
{
  "Mark McGwire": {
    "hr": 65,
    "avg": 0.278
  },
  "Sammy Sosa": {
    "hr": 63,
    "avg": 0.288
  }
}
```

### Nested
```json
{
  "Jack": {
    "id": 1,
    "name": "Franc",
    "salary": 25000,
    "hobby": ["a", "b"],
    "location": {
        "country": "A", "city": "A-A"
    }
  }
}
```


### Null

In JSON, `null` represents an empty value or a non-existent field.

#### Example:

```json
{
  "middleName": null,
  "previousAddress": null
}
```

Use `null` to denote the absence of a value or to clear an existing value in JSON data structures.


### Handling Dates in JSON

JSON does not have a built-in Date type. Dates are typically represented as strings, often in ISO 8601 format.

#### Format:
- **ISO 8601 Example**: `"2023-04-01T12:00:00Z"` for 1st April 2023, noon UTC.

#### Best Practices:
- **Always use strings to represent dates** in JSON and specify the format being used if not ISO 8601.
- **Convert to Date objects** in your code after parsing the JSON, if necessary.



## Access JSON in JavaScript 
### Access Object

```javascript
let myObject = {
  "name": "Jason",
  "last": "Doe",
  "age": 39,
  "gender": "M",
  "salary": 70000,
  "married": true
};
```
----

|                    |           |
|--------------------|-----------|
| `myObject.name`    | "Jason"   |
| `myObject["name"]` | "Jason"   |
| `myObject.age`     | 39        |
| `myObject.other`   | undefined |
| `myObject[0]`      | undefined |



### Access Nested
```javascript
let myObject = {
  "ref": {
    "name": 0,
    "last": 1,
    "age": 2,
    "gender": 3,
    "salary": 4,
    "married": 5
  },
  "jdoe": [
    "Jason",
    "Doe",
    39,
    "M",
    70000,
    true
  ],
  "jsmith": [
    "Tom",
    "Smith",
    42,
    "F",
    80000,
    true
  ]
};
```
----

|                          |                          |
|--------------------------|--------------------------|
| `myObject.ref.age`       | 2                        |
| `myObject["ref"]["age"]` | 2                        |
| `myObject.jdoe`          | ["Jason", "Doe", 39 ...] |
| `myObject.jsmith[3]`     | "F"                      |
| `myObject[1]`            | undefined                |



### Access Array of Objects
```javascript
let myArray = [
  {
    "name": "Jason",
    "last": "Doe",
    "age": 39,
    "gender": "M",
    "salary": 70000,
    "married": true
  },
  {
    "name": "Tom",
    "last": "Smith",
    "age": 42,
    "gender": "F",
    "salary": 80000,
    "married": true
  },
  {
    "name": "Amy",
    "last": "Burnquist",
    "age": 29,
    "gender": "F",
    "salary": 60000,
    "married": false
  }
];
```
----

|                     |                            |
|---------------------|----------------------------|
| `myArray[0]`        | `{`"name": "Jason", ...`}` |
| `myArray[1].name`   | "Tom"                      |
| `myArray[1][2]`     | 42                         |
| `myArray[3]`        | undefined                  |
| `myArray[3].gender` | TypeError: Cannot read...  |




### Access Array
```javascript
let myArray = [
  "Jason",
  "Doe",
  39,
  "M",
  70000,
  true
];
```
-----

|              |           |
|--------------|-----------|
| `myArray[1]` | "Doe"     |
| `myArray[5]` | true      |
| `myArray[6]` | undefined |

### JSON Parsing and Stringification

Convert between JSON strings and JavaScript objects using `JSON.parse()` and `JSON.stringify()`.

#### Parsing JSON:
- **To JavaScript Object**: `let obj = JSON.parse(jsonString);`

#### Stringifying JavaScript Object:
- **To JSON String**: `let jsonString = JSON.stringify(obj);`


### Accessing Deeply Nested JSON

Navigate through nested structures with dot notation or bracket notation for dynamic keys.

#### Example:
- **Dot Notation**: `let city = obj.user.address.city;`
- **Bracket Notation**: `let city = obj['user']['address']['city'];`

#### Tips:
- **Check for undefined**: Always validate parent objects before accessing child properties to avoid runtime errors.
- **Use optional chaining (?.)** in JavaScript for safer access: `let city = obj.user?.address?.city;`


## Useful tips and Links
### JSON Schema

Validate the structure of JSON data using JSON Schema, a vocabulary that allows you to annotate and validate JSON documents.

#### Key Points:
- **Define JSON Format**: Create schemas to describe your JSON format, including objects, arrays, and value types.
- **Validation**: Use JSON Schema to validate JSON data against your schema to ensure it meets expected formats and values.

#### Resources:
- **Official Site**: [JSON Schema](https://json-schema.org/)



### JSON Performance Considerations

Handling large JSON files efficiently is crucial for performance.

#### Tips:
- **Streaming**: Parse large JSON files with streaming to reduce memory usage.
- **Minification**: Minimize file size by removing unnecessary spaces, line breaks, and comments for production.
- **Batch Processing**: Process large JSON files in chunks to avoid blocking the main thread in applications.


### JSON Security

Secure handling of JSON is essential to protect against common vulnerabilities.

#### Key Points:
- **Avoid `eval()`**: Use `JSON.parse()` instead to parse JSON strings safely.
- **Sanitize Input**: Always validate and sanitize JSON data from untrusted sources to prevent injection attacks.

### Links
- [JSON](https://www.json.org/json-en.html)
- [JSON Editor Online](http://jsoneditoronline.org/)
- [Convert JSON Array to Markdown Table, CSV and more](https://tableconvert.com/json-to-markdown)#booleanThis comprehensive JSON Cheat Sheet is your go-to resource for mastering JSON, the lightweight, text-based data interchange format. From syntax basics, types, and examples to parsing and stringification in JavaScript, it covers essential aspects to enhance your data handling skills. Whether you're learning JSON for the first time or brushing up on specifics like encoding, security, and performance considerations, this cheat sheet offers succinct, actionable information to streamline your development process.
