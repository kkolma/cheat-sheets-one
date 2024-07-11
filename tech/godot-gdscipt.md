This Godot GDScript cheat sheet provides a quick reference to essential syntax and functionalities. It covers basic elements such as comments, output, and indentation, and dives into variable declaration, data structures, and operators. The guide also includes sections on control flow, loops, functions, and error handling, alongside classes, objects, and signals. With helpful examples and tips, this cheat sheet is a valuable resource for both beginners and experienced Godot developers. 

## Basic Syntax
### Comments

- Single-line comments: `# This is a single-line comment`
- Multi-line comments: For multi-line comments you need to prefix every line with `#` hash, sadly in GDScript there's no easier way. Be careful with `"""` three quotes `"""` while it looks like multi-line comments, it's actually a multi-line strings and will be silently executed by the interpreter!

```gdscript
"""
This is a multiline string, not a comment!
And thus it will be parsed by interpreter...
"""

# Now this
# is a multiline comments
# Interpreter will not read this
```

### Basic Output

To print output in GDScript, use the `print()` function:

```gdscript
print("Hello, Godot!")
```

### Indentation

GDScript uses indentation to define code blocks, just like Python:

```gdscript
func _init():
    pass
```

### Variables

In GDScript, variables can be declared using the `var` keyword. You can also specify the type of the variable using a colon (`:`) followed by the type name.

- Declare a variable: `var my_variable = 10`
- Change the value of a variable: `my_variable = 20`
- Declare a variable with a specific type: `var my_int: int = 5`

Here are some common data types in GDScript:

- `int`: Integer numbers
- `float`: Floating-point numbers
- `bool`: Boolean values (`true` or `false`)
- `String`: Text strings

```gdscript
var x: int = 42
var y: float = 3.14
var is_active: bool = true
var name: String = "https://godot.community"
```

### Arrays and Dictionaries

GDScript also provides built-in data structures like arrays and dictionaries:

- `Array`: Ordered list of elements
- `Dictionary`: Key-value pairs

```gdscript
var my_array: Array = [1, 2, 3, 4, 5]
var my_dict: Dictionary = {"key1": "value1", "key2": "value2"}
```

### Static Variables

Static variables belong to a class rather than an instance of the class. To define a static variable, use the `static` keyword:

- Declare a static variable: `static var my_static_variable = 30`
- Change the value of a static variable: `my_static_variable = 40`
- Since statics belong to the class, you can also use `MyClass.my_static_variable = 40`

### Constants

- Declare a constant: `const MY_CONSTANT = 100`

## Operators

### Arithmetic

- Addition: `a + b`
- Subtraction: `a - b`
- Multiplication: `a * b`
- Division: `a / b`
- Modulus: `a % b`
- Power: `a ** b`

### Comparison

- Equal: `a == b`
- Not equal: `a != b`
- Less than: `a < b`
- Less than or equal: `a <= b`
- Greater than: `a > b`
- Greater than or equal: `a >= b`

### Logical

- And: `a and b` or `a && b`
- Or: `a or b` or `a || b`
- Not: `not a` or `!a`

### Bitwise

- Bitwise AND: `a & b`
- Bitwise OR: `a | b`
- Bitwise XOR: `a ^ b`
- Bitwise NOT: `~a`
- Left shift: `a << b`
- Right shift: `a >> b`

### Assignment

- Assign: `a = b`
- Add and assign: `a += b`
- Subtract and assign: `a -= b`
- Multiply and assign: `a *= b`
- Divide and assign: `a /= b`
- Modulus and assign: `a %= b`
- Power and assign: `a **= b`
- Left shift and assign: `a <<= b`
- Right shift and assign: `a >>= b`
- Bitwise AND and assign: `a &= b`
- Bitwise OR and assign: `a |= b`
- Bitwise XOR and assign: `a ^= b`

## Variable Typing

### Dynamic Typing

In GDScript, variables are dynamically typed by default, meaning their type is interchangeable at runtime. For example:

```gdscript
var my_variable = 10
my_variable = "Hello, GDScript!"  # This is allowed
```

### Static Typing

Static typing can be used to explicitly specify the type of a variable, meaning their type is not interchangeable at runtime. This can help catch potential bugs and improve code readability:

```gdscript
var my_int: int = 5
my_int = "Hello, GDScript!"  # This will cause an error
```

Static type can also be inferred by using `:=` followed by value. Be careful when using this though, sometimes verbosity is better.

```gdscript
var my_int := 5
my_int = "Hello World"  # Error, because my_int has been statically inferred as int
```


## Conditional statements

### If

The `if` statement is used to execute a block of code if a certain condition is true:

```gdscript
if x > 0:
    print("x is positive")
```

### Else

The `else` statement is used to execute a block of code if the condition in the `if` statement is false:

```gdscript
if x > 0:
    print("x is positive")
else:
    print("x is not positive")
```

### Elif

The `elif` (short for "else if") statement is used to test multiple conditions in a single `if` statement:

```gdscript
if x > 0:
    print("x is positive")
elif x < 0:
    print("x is negative")
else:
    print("x is zero")
```

## Loops

### For

The `for` loop is used to iterate over a sequence, such as an array or a range of numbers:

```gdscript
for i in range(5):
    print(i)  # Prints 0, 1, 2, 3, 4

for item in my_array:
    print(item)  # Prints each item in my_array
```

### While

The `while` loop is used to repeatedly execute a block of code as long as a certain condition is true:

```gdscript
var i = 0
while i < 5:
    print(i)  # Prints 0, 1, 2, 3, 4
    i += 1
```

### Break and Continue

The `break` statement is used to exit a loop prematurely:

```gdscript
for i in range(10):
    if i == 5:
        break
    print(i)  # Prints 0, 1, 2, 3, 4
```

The `continue` statement is used to skip the rest of the current iteration and proceed to the next one:

```gdscript
for i in range(5):
    if i == 2:
        continue
    print(i)  # Prints 0, 1, 3, 4
```

## Functions
### Defining functions

To define a function, use the `func` keyword followed by the function name and a pair of parentheses:

```gdscript
func my_function():
    print("Hello, GDScript!")
```

### Built-in functions

GDScript comes with a variety of built-in functions that you can use in your code. Some examples include:

- `print()`: Prints a message to the console
- `randi()`: Returns a random integer
- `len()`: Returns the length of a sequence (e.g., an array or a string)

### Function arguments

Functions can take input in the form of arguments. To define a function with arguments, include the argument names inside the parentheses:

```gdscript
func add(a, b):
    return a + b
```

You can also define the types of the arguments, it will spit out an error if you try to pass different types to the arguments.

```gdscript
func add(a: int, b: int):
    return a + b
```

### Return values

Functions can return a result using the `return` keyword:

```gdscript
func add(a, b):
    return a + b

var result = add(2, 3)  # result is 5
```

You can also define the type of the returned value by appending `-> ReturnType` to the function declaration, it will spit out an error if you try to return something that isn't the correct type.

```gdscript
# Returns integer
func add(a: int, b: int) -> int:
    return a + b

# This won't work
func add(a, b) -> int:
    return "Hello"
```

### Optional argument values

Functions can have optional argument values

 by assigning it at the definition:

```gdscript
func multiply(a: int, b: int = 2) -> int:
    return a * b

var result = multiply(2, 3)  # result is 6
var result = multiply(4)  # result is 8
```

**Note**: Optional arguments can only be positioned after you've defined all mandatory arguments.

```gdscript
# Valid, optional placed last
func sum(a: int, b: int, c: int = 0) -> int:
    return a + b + c

# Invalid, can't have optional before mandatory
func sum(a: int, b: int = 0, c: int) -> int:
    return a + b + c
```

### Static Functions

Static functions are functions that belong to a class rather than an instance of the class. To define a static function, use the `static` keyword:

```gdscript
class_name  MyClass extends Node

static func my_static_function():
    print("This is a static function.")

func _init() -> void:
    my_static_function()
    MyClass.my_static_function()
```

Since statics belong to the class, you can use `MyClass.my_static_function()` to invoke it.

## Classes and Objects
### Defining Classes

To define a class, simply create a new script file (e.g., `my_class.gd`). The name of the file should represent the name of the class. Create a new file called `player.gd` with the following content:

```gdscript
class_name Player

var health: int = 100
var name: String = "Unnamed"

func take_damage(amount: int):
    health -= amount
    if health <= 0:
        print("Player", name, "has died!")
```

### Creating Object

```gdscript
var player = Player.new()
player.name = "John Doe"
player.take_damage(50)
```

### Properties

Properties are variables that belong to a class or an object. They can be used to store data or state:

```gdscript
class MyClass:
    var my_property = 0
```

### Methods

Methods are functions that belong to a class or an object. They can be used to perform actions or manipulate data:

```gdscript
class MyClass:
    func my_method():
        print("Hello, GDScript!")
```

### Inheritance

Inheritance is a way for one class to inherit the properties and methods of another class. To inherit from another class, use the `extends` keyword:

```gdscript
# Derived class
class_name DerivedClass extends MyBaseClass

func my_method():
    print("Hello from the derived class!")
```

### Constructors

Constructors are special methods that are called when an object is initialized. In GDScript, the constructor is named `_init`:

```gdscript
class MyClass:
    func _init():
        print("Object initialized!")
```

## Signals and Events
### Defining signals
Signals are a way for objects to communicate with each other without relying on direct references. They can be used to decouple your code and make it more modular. Let's learn how to work with signals and events in GDScript. To define a signal, use the `signal` keyword followed by the signal name:

```gdscript
signal my_signal
```

### Emitting signals

To emit a signal, you can use the `emit_signal` method:

```gdscript
emit_signal("my_signal")
```

However, it's better to ditch those strings, by simply calling emit method inside the signal directly:

```gdscript
my_signal.emit()
```

### Connecting signals to functions

Signals are a way to communicate between objects in Godot. They allow you to decouple your code and create more modular systems.

To connect a signal to a function, use the `connect` method:

```gdscript
my_object.my_signal.connect(on_my_signal)

func on_my_signal():
    print("Signal received!")
```

There are actually four ways to connect signals, however, this is the recommended approach, instead of the other one (That might more error prone).

## Error Handling
### Assert

The `assert` statement is used to check if a condition is true, and if not, raise an error:

```gdscript
assert(x > 0, "x must be positive")
```

**Note**: `assert` is a utility function meant for unit tests. Code inside assert is only executed in debug builds or when running the project from the editor.

### Try, Catch, and Throw

GDScript does not have built-in support for try-catch blocks. There are many godot-proposals from people asking for it, however, It has already been stated that try-catch will never come into gdscript.

Quoting from Juan in [his post](https://github.com/godotengine/godot/issues/3516#issuecomment-177152034):

> Exceptions won't happen. Godot is designed for things to keep working even if state is inconsistent, while at the same time reporting errors

## File I/O
### Writing a file

To write to a file, use the `store_string`, `store_line` or other `store_*` methods:

```gdscript
var player_name = "Septian"
var file = FileAccess.open("user://save_game.dat", FileAccess.WRITE)
file.store_string(player_name)
```

### Reading and writing

To read from a file, use the `get_as_text` or other `get_*` method:

```gdscript
var file = FileAccess.open("user://save_game.dat", FileAccess.READ)
var player_name = file.get_as_text()
print(player_name)
```

### Closing files

To close a file, use the `close` method:

```gdscript
file.close()
```

`FileAccess` will automatically close the file when it goes out of scope or is set to null. However, it's better to be explicit when handling with I/O.

## Other
### String manipulation

- String interpolation:

```gdscript
var result = "The %s has defeated the %s in %s" % ["Player", "Boss", "Combat"]
print(result)
# Will print:
# The Player has defeated the Boss in Combat
```

- Concatenate strings: `var result = "Hello, " + "GDScript!"`
- Format strings: `var result = "Hello, %s!" % "GDScript"`
- Split strings: `var words = "Hello, GDScript!".split(", ")`

### Array and Dictionary operations

- Add an item to an array: `my_array.append(item)`
- Remove an item from an array: `my_array.erase(item)`
- Get the length of an array: `var length = my_array.size()`
- Check if a key exists in a dictionary: `if my_dict.has(key):`

### Type casting

- Cast a value to a specific type: `var my_int = int("42")`

### Debugging

- Print a message to the console: `print("Hello, GDScript!")`
- Set a breakpoint: `breakpoint`

## Useful Resources

### Useful Tips and Tricks

Here are some handy tips and tricks to help you write better GDScript:

- Use clear and descriptive variable and function names
- Keep your functions short and focused
- Use comments to explain complex or important code
- Follow the [GDScript style guide](https://godot.community/topic/27/gdscript-coding-conventions-best-practices-for-readable-and-maintainable-code)
- Follow the [GDScript code ordering](https://godot.community/topic/41/gdscript-best-practices-for-organized-code)

### Resources

To learn more about GDScript and the Godot game engine, check out these great resources:

- [Ask Godot Community](https://godot.community/category/22/ask)
- [Beginner's Corners](https://godot.community/category/24/beginner-s-corner)
- [Tutorials tagged posts](https://godot.community/tags/tutorial)
