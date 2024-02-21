This comprehensive Lua Cheat Sheet offers a quick reference to the essentials of Lua programming, including syntax for comments, variables, data types, operators, control structures, functions, tables, standard libraries, advanced features like metatables, modules, and coroutines, as well as practical tips for effective coding. Designed for both beginners and experienced developers, it provides the foundational knowledge needed to start coding in Lua and serves as a handy guide for quick lookups and refresher points.

## Fundamentals
### Comments
* Single-line comment: 
	* `-- This is a single-line comment`
* Multi-line block comment:
	* `--[[ This is a multi-line`
	* `comment ]]`
* In-line block comment:
	* `t = {1, 2, --[[in-line block comment]] 3}`
* Block comment that contains']]':
	* `--[=[ Block comment that contains "]]". ]=]`

### Variables & Scope
- Global variables: `varName = value`
- Local variables: `local varName = value`
- Example:
```
x = 1 -- global variable
local function equal(z)
...
local x = x -- local x = global x
...
end
```

### Data Types
- Nil: `nil`
- Boolean: `true`, `false`
- Number: `123`, `4.56`
- String: `"Hello"`, `'World'`
- Function: `function() end`
- Table: `{}` (used for arrays, dictionaries, objects)
- Thread: coroutine functions
- Userdata: custom C data types

## Operators
### Arithmetic operators
- Add: `x + y'
- Substract: `x - y`
- Multiply: `x * y`
- Divide: `x / y`
- Integer divide: `x // y`
- Reminder of Division: `x % y`
- Exponentiate: `x^y`

### Relational operators
- Is a equal to b?: `a == b`
- Is a not equal to b?: `a ~= b`
- a is less than b?: `a < b`
- a is less than or equal b?: `a <= b`
- a is greater than or equal a?: `a > b`
- a is greater than or equal a?: `a >= b`
Returns a boolean.

### Logical Operators
- `not a`: It negates the boolean value of `a`.
- `a and b`: This operator returns `a` if `a` is false; otherwise, it returns `b`. It is used to check if both conditions `a` and `b` are true.
- `a or b`: This operator returns `a` if `a` is true; otherwise, it returns `b`. It is useful for selecting the first true value between `a` and `b`.

### Bitwise Operators
- Bitwise AND:
  - `x & y` (Lua 5.3, 5.4)
  - `bit32.band(x, y)` (Lua 5.2)
- Bitwise OR:
  - `x | y` (Lua 5.3, 5.4)
  - `bit32.bor (x, y)` (Lua 5.2)
- Bitwise XOR:
	- `x ~ y` (Lua 5.3, 5.4)
	- `bit32.bxor(x, y)` (Lua 5.2)
- Bitwise NOT:
	- `~x` (Lua 5.3, 5.4)
	- `bit32.bnot(x)` (Lua 5.2)
- Shift:
	- `x << y` (Lua 5.3, 5.4)
	- `bit32.lshift(x, y)` (Lua 5.2)
	- `x >> y` (Lua 5.3, 5.4)
	- `bit32.rshift(x, y)` (Lua 5.2)

### Other Operators
- Returns strings or numbers a and b concatenated
together into a new string: `a .. b`
- Returns the length of value v: `#v`
- Function calls:
	- `f([expr1, expr2, …, exprN])`
	- `f{…}`
	- `f"string" or f'string' or f[[string]]`
- Retrieves the value in table t:
	- `t[key]`
	- `t.name`

## Statements / Control Structures
### If-Then-Else
```
if condition then
-- code
elseif anotherCondition then
-- code
else
-- code
end
```

### For Loops
**For (numeric):**
```
for i=1, 10 do
-- code
end
```

**For (generic):**
```
for key, value in pairs(table) do
-- code
end
```

### While/Repeat Loops
**While:**
```
while condition do
-- code
end
```

**Repeat-Until:**
```
repeat
-- code
until condition
```

### Labels and Goto
- Label: `::label::`
- Goto label: `goto label` 

## Functions
### Basics
- Example1: 
````
function getSum(num1, num2)
  return num1 + num2
end
````

- Usage:
`print(string.format("5 + 2 = %d", getSum(5,2)))`

- Example2:
````
function splitStr(theString)

  stringTable = {}
  local i = 1

  -- Cycle through the String and store anything except for spaces
  -- in the table
  for str in string.gmatch(theString, "[^%s]+") do
    stringTable[i] = str
    i = i + 1
  end
````

### Multiple Values
- Return multiple values:
````
return stringTable, i
end
````

- Receive multiple values:

`splitStrTable, numOfStr = splitStr("The Turtle")`

````
for j = 1, numOfStr do
  print(string.format("%d : %s", j, splitStrTable[j]))
end
````

### Variadic Function
- Variadic Function recieve unknown number of parameters
````
function getSumMore(...)
  local sum = 0

  for k, v in pairs{...} do
    sum = sum + v
  end
  return sum
end
````

- Usage:
````
io.write("Sum : ", getSumMore(1,2,3,4,5,6), "\n")
````

### Invoking functions
````
print()
print("Hi")
````
- You can omit parentheses if the argument is one string or table literal:
````
print "Hello World" <--> print("Hello World")
dofile 'a.lua' <--> dofile ('a.lua')
print [[a multi-line <--> print([[a multi-line
message]] message]])
f{x=10, y=20} <--> f({x=10, y=20})
type{} <--> type({})
````

### Closure
- A Closure is a function that can access local variables of an enclosing function:
````
function outerFunc()
  local i = 0
  return function()
    i = i + 1
    return i
  end
end
````


## Tables
### Creating Tables
* Empty table: `empty = {}`
* With values: `list = {1, 2, 3}`
* Dictionary: `dict = {["a"] = 1, ["b"] = 2, ["c"] = 3}`
* Mixed content: `mix = {[0] = 0, 1, 2, 3, a = 1, b = 2, c = 3}`

### Accessing Values
* Array-style: `local value = t[1]`
* Dictionary-style: `local value = t.key`

### Setting Values
* `t[1] = "a"`
* `t.key = "value"`

### Iterating Over Tables
* Pairs (for dictionaries):
```
for key, value in pairs(t) do
-- code
end
```
* ipairs (for arrays):
```
for index, value in ipairs(t) do`
`-- code`
`end
```

### Lookups

`mytable = { x = 2, y = function() .. end }`
- The same:
	- `mytable.x`
	- `mytable['x']`

- Syntactic sugar, these are equivalent:
	- `mytable.y(mytable)` = `mytable:y()`
	- `mytable.y(mytable, a, b) = 'mytable:y(a, b)`
	- `function X:y(z) .. end` = `function X.y(self, z) .. end`

## Standard Libraries
### String Library
* Concatenation: `"Hello " .. "World"`
* Length: `#str`
* Find: `string.find(str, substring)`
* Replace: `string.gsub(str, pattern, replacement)`

### Math Library
* Basic operations: `+`, `-`, `*`, `/`, `//`, `%`
* Power: `math.pow(x, y)` or `x^y`
* Square root: `math.sqrt(x)`
* Trigonometry: `math.sin(x)`, `math.cos(x)`,` math.tan(x)`

### Table Library
* Insert:`table.insert(t, value)`
* Remove: `table.remove(t, position)`
* Sort: `table.sort(t, compareFunction)`

### Input and Output
* Read from standard input: `io.read()`
* Print to standard output: `print("Hello, World!")`
* Open a file: local file = `io.open(filename, mode)`


## Advanced

### Metatables
Metatables in Lua allow you to change the behavior of tables.
#### Setting a Metatable
```lua
local myTable = {}
local myMetatable = {}
setmetatable(myTable, myMetatable)
```

#### Getting a Metatable
`local mt = getmetatable(myTable)`

### Metamethods
Metamethods are special keys in a metatable that correspond to operator overloads and other behavior modifications.
- `__index`: Controls behavior when accessing missing keys. Can be a function or a table.
- `__newindex`: Controls behavior when setting values to missing keys.
- `__call`: Allows the table to be called as a function.
- `__add, __sub, __mul, __div, __mod, __pow, __unm`: Define behavior for arithmetic operations.
- `__eq, __lt, __le`: Define behavior for equality and relational operations.
- `__tostring`: Defines how a table is converted to a string, useful for debugging.

### Modules
A Module is like a library full of functions and variables.

- Use require to gain access to the functions in the module:
`convertModule = require("convert")`

- Execute the function in the module:
`print(string.format("%.3f cm", convertModule.ftToCm(12)))`

-Module search path:
`package.path = package.path .. ";/path/to/your/modules/?.lua"`

### Coroutines
Coroutines are like threads except that they can't run in parallel (status: running, susepnded, dead or normal).

- Use create to create one that performs some action
````
co = coroutine.create(function()
  for i = 1, 10, 1 do
  print(i)
  print(coroutine.status(co))
  if i == 5 then coroutine.yield() end
  end end)
````
- They start off with the status suspended:
`print(coroutine.status(co))`
- Call for it to run with resume during which the status changes to running:
`coroutine.resume(co)`
- After execution it has the status of dead:
`print(coroutine.status(co))`


## Useful tips
### Tips
1.  **Local Variables**: Use `local` variables whenever possible to improve performance and avoid polluting the global namespace.
2.  **Garbage Collection**: Lua's garbage collector will automatically free up memory, but you can also manually control it with `collectgarbage()` for optimization.
3.  **Error Handling**: Use `pcall` (protected call) to safely execute a function and catch potential errors without causing a program crash.
4.  **Modules and Packages**: Organize code into modules and packages for better code management. Use `require` to include them without duplicating code.
ustom iterator functions.

### Links / References
* [Lua Quick Reference](https://orbitalquark.github.io/lua-quick-reference/)
* Nilesh Tawari's Lua reference guide
* [Lua Manual](https://www.lua.org/manual/)
* [Lua 5.4 Reference Manual](https://devdocs.io/lua~5.4/)
