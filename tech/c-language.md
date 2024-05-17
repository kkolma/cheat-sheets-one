This C language  cheat sheet provides a quick reference guide to the essential syntax, operators, control flow, functions, data structures, and standard library functions in C. Perfect for both beginners and experienced programmers, it covers everything from basic syntax and operators to advanced topics like dynamic memory allocation and file I/O. Keep this handy for efficient coding and problem-solving in C.

## Basic Syntax and Structure
### Hello World Program
```c
#include <stdio.h>

int main() {
    printf("Hello, World!");
    return 0;
}
```

### Basic Structure of a C Program
- Include Headers
- Define Constants and Macros
- Declare Functions
- Main Function
- Other Functions

### Comments
```c
// Single-line comment

/* 
Multi-line comment 
*/
```

## Data Types and Variables
### Primitive Data Types
- int
- char
- float
- double

### Variable Declaration and Initialization
```c
int a = 10;
char b = 'c';
float c = 3.14;
double d = 3.14159;
```

### Constants
```c
#define PI 3.14
const int a = 10;
```

## Operators

### Arithmetic Operators
- `+` Addition: `a + b`
- `-` Subtraction: `a - b`
- `*` Multiplication: `a * b`
- `/` Division: `a / b`
- `%` Modulus: `a % b`
- `++` Increment: `a++`
- `--` Decrement: `a--`

### Relational Operators
- `==` Equal to: `a == b`
- `!=` Not equal to: `a != b`
- `>` Greater than: `a > b`
- `<` Less than: `a < b`
- `>=` Greater than or equal to: `a >= b`
- `<=` Less than or equal to: `a <= b`

### Logical Operators
- `&&` Logical AND: `a && b`
- `||` Logical OR: `a || b`
- `!` Logical NOT: `!a`

### Bitwise Operators
- `&` AND: `a & b`
- `|` OR: `a | b`
- `^` XOR: `a ^ b`
- `~` NOT: `~a`
- `<<` Left shift: `a << 2`
- `>>` Right shift: `a >> 2`

### Assignment Operators
- `=` Assign: `a = b`
- `+=` Add and assign: `a += b`
- `-=` Subtract and assign: `a -= b`
- `*=` Multiply and assign: `a *= b`
- `/=` Divide and assign: `a /= b`
- `%=` Modulus and assign: `a %= b`
- `&=` AND and assign: `a &= b`
- `|=` OR and assign: `a |= b`
- `^=` XOR and assign: `a ^= b`
- `<<=` Left shift and assign: `a <<= b`
- `>>=` Right shift and assign: `a >>= b`

### Miscellaneous Operators
- `sizeof` Size of: `sizeof(a)`
- `? :` Ternary: `(a > b) ? a : b`

### Examples
```c
int a = 10, b = 5, result;
result = a + b;     // Addition
result = a - b;     // Subtraction
result = a * b;     // Multiplication
result = a / b;     // Division
result = a % b;     // Modulus
result = a & b;     // Bitwise AND
result = a | b;     // Bitwise OR
result = a ^ b;     // Bitwise XOR
result = ~a;        // Bitwise NOT
result = a << 1;    // Left shift
result = a >> 1;    // Right shift
a += b;             // Addition assignment
b -= a;             // Subtraction assignment
result = (a > b) ? a : b; // Ternary operator
```

## Control Flow
### Conditional Statements
```c
if (condition) {
    // code
} else {
    // code
}

switch (expression) {
    case constant1:
        // code
        break;
    case constant2:
        // code
        break;
    default:
        // code
}
```

### Loops
```c
for (initialization; condition; increment) {
    // code
}

while (condition) {
    // code
}

do {
    // code
} while (condition);
```

### Break and Continue
```c
break;
continue;
```

### Goto Statement
```c
goto label;
label: // code
```

## Functions
### Function Declaration and Definition
```c
returnType functionName(parameter1, parameter2, ...) {
    // code
    return value;
}
```

### Function Call
```c
functionName(arg1, arg2, ...);
```

### Return Statement
```c
return value;
```

### Parameter Passing
- By value
- By reference

### Recursion
```c
int factorial(int n) {
    if (n == 0) return 1;
    return n * factorial(n - 1);
}
```

## Arrays and Strings
### One-dimensional Arrays
```c
int arr[10];
```

### Multidimensional Arrays
```c
int arr[3][4];
```

### String Handling Functions
```c
strcpy(destination, source);
strcat(destination, source);
strlen(string);
```

### Array of Strings
```c
char *arr[] = {"string1", "string2"};
```

## Pointers
### Pointer Basics
```c
int *ptr;
```

### Pointer Arithmetic
- `ptr++` `ptr--` `ptr+5` `ptr-5`

### Pointers and Arrays
```c
int arr[5];
int *ptr = arr;
```

### Pointers to Pointers
```c
int **ptr;
```

### Function Pointers
```c
void (*funcPtr)(int, int);
```

## Structures and Unions
### Defining Structures
```c
struct StructureName {
    type member1;
    type member2;
    // ...
};
```

### Accessing Structure Members
```c
struct StructureName s;
s.member1 = value;
```

### Structure Arrays
```c
struct StructureName arr[10];
```

### Nested Structures
```c
struct Outer {
    struct Inner {
        // ...
    } inner;
};
```

### Unions
```c
union UnionName {
    type member1;
    type member2;
    // ...
};
```

## Dynamic Memory Allocation
### malloc(), calloc(), realloc(), free()
```c
ptr = malloc(size);
ptr = calloc(num, size);
ptr = realloc(ptr, newSize);
free(ptr);
```

### Memory Leaks and Management
- Always free allocated memory

## File I/O
### File Handling Functions
```c
FILE *fptr;
fptr = fopen("filename", "mode");
fclose(fptr);
fread(buffer, size, count, fptr);
fwrite(buffer, size, count, fptr);
```

### File Modes
- `"r"` `"w"` `"a"` `"r+"` `"w+"` `"a+"`

### Reading and Writing Files
```c
fscanf(fptr, "format", &variable);
fprintf(fptr, "format", variable);
```

## Preprocessors and Macros
### #define and #undef
```c
#define NAME value
#undef NAME
```

### #include
```c
#include <header.h>
#include "file.h"
```

### Conditional Compilation
```c
#ifdef MACRO
    // code
#endif

#ifndef MACRO
    // code
#endif

#if condition
    // code
#elif condition
    // code
#else
    // code
#endif
```

### Macros with Arguments
```c
#define MACRO(arg1, arg2) (arg1 + arg2)
```

## Standard Library Functions

### stdio.h
- `printf` - formatted output to stdout
- `scanf` - formatted input from stdin
- `fprintf` - formatted output to a file
- `fscanf` - formatted input from a file
- `sprintf` - formatted output to a string
- `sscanf` - formatted input from a string
- `fopen` - open a file
- `fclose` - close a file
- `fgets` - read a string from a file
- `fputs` - write a string to a file
- `fgetc` - get a character from a file
- `fputc` - write a character to a file
- `feof` - check for end-of-file
- `ferror` - check for file error

### stdlib.h
- `malloc` - allocate memory
- `calloc` - allocate and zero-initialize memory
- `realloc` - reallocate memory
- `free` - free allocated memory
- `atoi` - convert string to integer
- `atof` - convert string to float
- `atol` - convert string to long
- `abs` - compute absolute value
- `rand` - generate random number
- `srand` - seed the random number generator
- `qsort` - quick sort
- `bsearch` - binary search
- `exit` - terminate the program
- `system` - execute a system command

### string.h
- `strlen` - get string length
- `strcmp` - compare two strings
- `strncmp` - compare a portion of two strings
- `strcpy` - copy a string
- `strncpy` - copy a portion of a string
- `strcat` - concatenate two strings
- `strncat` - concatenate a portion of a string
- `strstr` - locate a substring
- `strchr` - locate the first occurrence of a character
- `strrchr` - locate the last occurrence of a character
- `strtok` - tokenize a string
- `strdup` - duplicate a string
- `memcpy` - copy memory area
- `memmove` - move memory area
- `memset` - fill memory with a constant byte
- `memcmp` - compare two memory areas

### math.h
- `sqrt` - compute square root
- `pow` - compute power
- `exp` - compute exponential
- `log` - compute natural logarithm
- `log10` - compute common logarithm
- `sin` - compute sine
- `cos` - compute cosine
- `tan` - compute tangent
- `asin` - compute arc sine
- `acos` - compute arc cosine
- `atan` - compute arc tangent
- `atan2` - compute arc tangent with two arguments
- `ceil` - compute ceiling
- `floor` - compute floor
- `fabs` - compute absolute value of a floating-point number

### time.h
- `time` - get current time
- `clock` - get processor time
- `difftime` - compute difference between two times
- `mktime` - convert broken-down time to calendar time
- `asctime` - convert time to a string
- `ctime` - convert time to a string
- `gmtime` - convert time to Coordinated Universal Time (UTC)
- `localtime` - convert time to local time
- `strftime` - format time as a string

## Miscellaneous
### Command Line Arguments
```c
int main(int argc, char *argv[]) {
    // code
}
```

### Inline Functions
```c
inline returnType functionName(parameters) {
    // code
}
```

### Volatile Keyword
```c
volatile int var;
```

### Typedef
```c
typedef existingType newTypeName;
```

## Best Practices and Tips

### Code Readability
- **Indentation:** Use consistent indentation to make code more readable.
- **Naming Conventions:** Use meaningful variable and function names. Follow conventions like camelCase for variables and PascalCase for functions.
- **Spacing:** Use spaces around operators and after commas for better readability.

### Commenting and Documentation
- **Single-line Comments:** Use `//` for brief comments.
- **Multi-line Comments:** Use `/* */` for detailed explanations.
- **Function Comments:** Describe the purpose, parameters, and return value of functions.
- **Inline Comments:** Explain complex logic within the code.

### Debugging Tips
- **Use a Debugger:** Utilize tools like gdb to step through your code and inspect variables.
- **Print Statements:** Use `printf` to print variable values and checkpoints in the code.
- **Check Compiler Warnings:** Always compile with `-Wall` to enable all warnings and fix them.

### Optimization Techniques
- **Avoid Unnecessary Calculations:** Store repeated calculations in a variable.
- **Efficient Algorithms:** Choose appropriate algorithms and data structures for the task.
- **Memory Management:** Free dynamically allocated memory to avoid leaks.

### Useful Links
1. [C Programming - GeeksforGeeks](https://www.geeksforgeeks.org/c-programming-language/)
2. [Learn C - TutorialsPoint](https://www.tutorialspoint.com/cprogramming/index.htm)
3. [The C Programming Language - Cprogramming.com](https://www.cprogramming.com/tutorial/c-tutorial.html)
4. [C Standard Library - cppreference.com](https://en.cppreference.com/w/c)
5. [GNU C Library Documentation](https://www.gnu.org/software/libc/manual/)
