This **Python String Methods Cheat Sheet** provides a comprehensive list of built-in string methods in Python, organized by category for easy reference. Each method includes a brief description and a simple example to illustrate its usage. Whether you're *formatting, searching, modifying, or analyzing strings*, this cheat sheet offers quick access to the tools you need. Ideal for both beginners and experienced programmers, it serves as a handy guide for efficient string manipulation in Python.

## Case Conversion

### `str.capitalize()`
Capitalizes the first character.
```python
"hello world".capitalize()
```
Output: "Hello world"

### `str.lower()`
Converts all characters to lowercase.
```python
"Hello World".lower()
```
Output: "hello world"

### `str.upper()`
Converts all characters to uppercase.
```python
"Hello World".upper()
```
Output: "HELLO WORLD"

### `str.title()`
Converts the first character of each word to uppercase.
```python
"hello world".title()
```
Output: "Hello World"

### `str.swapcase()`
Swaps the case of all characters.
```python
"Hello World".swapcase()
```
Output: "hELLO wORLD"

### `str.casefold()`
Converts the string to casefolded (lowercase) version for case-insensitive comparisons.
```python
"Hello World".casefold()
```
Output: "hello world"

## String Formatting

### `str.center(width, fillchar=' ')`
Centers the string.
```python
"hello".center(10, '-')
```
Output: "--hello---"

### `str.ljust(width, fillchar=' ')`
Left-justifies the string.
```python
"hello".ljust(10, '-')
```
Output: "hello-----"

### `str.rjust(width, fillchar=' ')`
Right-justifies the string.
```python
"hello".rjust(10, '-')
```
Output: "-----hello"

### `str.zfill(width)`
Pads the string with zeros on the left.
```python
"42".zfill(5)
```
Output: "00042"

### `str.format(*args, **kwargs)`
Formats the string.
```python
"Hello, {}!".format("world")
```
Output: "Hello, world!"

### `str.format_map(mapping)`
Formats the string using a dictionary.
```python
data = {"name": "world"}
"Hello, {name}!".format_map(data)
```
Output: "Hello, world!"

## Search and Replace

### `str.find(sub, start=0, end=len(str))`
Returns the lowest index of the substring.
```python
"hello world".find("world")
```
Output: 6

### `str.rfind(sub, start=0, end=len(str))`
Returns the highest index of the substring.
```python
"hello world world".rfind("world")
```
Output: 12

### `str.index(sub, start=0, end=len(str))`
Same as `find()` but raises `ValueError` when the substring is not found.
```python
"hello world".index("world")
```
Output: 6

### `str.rindex(sub, start=0, end=len(str))`
Same as `rfind()` but raises `ValueError` when the substring is not found.
```python
"hello world world".rindex("world")
```
Output: 12

### `str.replace(old, new, count=-1)`
Replaces occurrences of a substring with another substring.
```python
"hello world".replace("world", "Python")
```
Output: "hello Python"

## Splitting and Joining

### `str.split(sep=None, maxsplit=-1)`
Splits the string into a list.
```python
"hello world".split()
```
Output: ["hello", "world"]

### `str.rsplit(sep=None, maxsplit=-1)`
Splits the string into a list, starting from the right.
```python
"hello world".rsplit()
```
Output: ["hello", "world"]

### `str.splitlines(keepends=False)`
Splits the string at line breaks.
```python
"hello\nworld".splitlines()
```
Output: ["hello", "world"]

### `str.join(iterable)`
Joins an iterable of strings.
```python
"-".join(["hello", "world"])
```
Output: "hello-world"

## Trimming and Stripping

### `str.strip(chars=None)`
Removes leading and trailing characters.
```python
"  hello  ".strip()
```
Output: "hello"

### `str.lstrip(chars=None)`
Removes leading characters.
```python
"  hello  ".lstrip()
```
Output: "hello  "

### `str.rstrip(chars=None)`
Removes trailing characters.
```python
"  hello  ".rstrip()
```
Output: "  hello"

## Character Classification

### `str.isalnum()`
Returns `True` if all characters are alphanumeric.
```python
"hello123".isalnum()
```
Output: True

### `str.isalpha()`
Returns `True` if all characters are alphabetic.
```python
"hello".isalpha()
```
Output: True

### `str.isdigit()`
Returns `True` if all characters are digits.
```python
"12345".isdigit()
```
Output: True

### `str.isnumeric()`
Returns `True` if all characters are numeric.
```python
"12345".isnumeric()
```
Output: True

### `str.isdecimal()`
Returns `True` if all characters are decimals.
```python
"12345".isdecimal()
```
Output: True

### `str.islower()`
Returns `True` if all characters are lowercase.
```python
"hello".islower()
```
Output: True

### `str.isupper()`
Returns `True` if all characters are uppercase.
```python
"HELLO".isupper()
```
Output: True

### `str.isspace()`
Returns `True` if all characters are whitespace.
```python
"   ".isspace()
```
Output: True

### `str.istitle()`
Returns `True` if the string is in title case.
```python
"Hello World".istitle()
```
Output: True

## Encoding and Decoding

### `str.encode(encoding='utf-8', errors='strict')`
Encodes the string to bytes.
```python
"hello".encode()
```
Output: b'hello'

### `bytes.decode(encoding='utf-8', errors='strict')`
Decodes bytes to a string.
```python
b'hello'.decode()
```
Output: "hello"

## String Testing

### `str.startswith(prefix, start=0, end=len(str))`
Returns `True` if the string starts with the specified prefix.
```python
"hello world".startswith("hello")
```
Output: True

### `str.endswith(suffix, start=0, end=len(str))`
Returns `True` if the string ends with the specified suffix.
```python
"hello world".endswith("world")
```
Output: True

## Other Utility Methods

### `str.count(sub, start=0, end=len(str))`
Counts the occurrences of a substring.
```python
"hello world".count("o")
```
Output: 2

### `str.expandtabs(tabsize=8)`
Expands tabs into spaces.
```python
"hello\tworld".expandtabs(4)
```
Output: "hello   world"

### `str.partition(sep)`
Splits the string into three parts around a separator.
```python
"hello world".partition(" ")
```
Output: ('hello', ' ', 'world')

### `str.rpartition(sep)`
Splits the string into three parts, starting from the right.
```python
"hello world world".rpartition(" ")
```
Output: ('hello world', ' ', 'world')

### `str.maketrans(x, y=None, z=None)`
Creates a translation table.
```python
table = str.maketrans("abc", "123")
```

### `str.translate(table)`
Translates the string using a translation table.
```python
table = str.maketrans("abc", "123")
"abc".translate(table)
```
Output: "123"
