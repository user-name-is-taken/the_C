# ch1 notes

# 1.1 Getting started

- To install the gcc compiler on windows, install chocolatey [which you can do without admin access](https://chocolatey.org/docs/installation#non-administrative-install), then run `choco install mingw`.
- You can then run `.c` files in vscode with the [run code extension](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner#:~:text=To%20run%20code%3A,Code%20in%20editor%20context%20menu).
- C programs start executing from `main()`
- `#include <stdio.h>` includes the standard I/O library described in ch 7 and appendix B

- common escape sequences (see 2.3 for more):
  - `\n` for newline
  - `\t` for tab
  - `\b` for backspace
  - `\"` for double quote
  - `\\` for the backslash itself

- note, the `\` can only be used with valid escape sequences.

# 1.2 Variables and Arithmetic Expressions

- In this section, we will explore concepts from [temps.c](./examples/temps.c)
- Comments can use `//` for single line or `/* ... */` for multi line

- C datatypres for values:
  - __char__: character - a single byte
  - __short__: short int
  - __long__: a long int
  - __double__: double-precision floating point
  - __int__
  - __float__

- Sizes of the above datatypes are machine dependent
- Values can be organized into __arrays__, __structures__ and __unions__. __Pointers__ reference values, and functions can return a value.
- Values are defined in __declarations__ and given a value in __assignments__. This is often done in the same line.
- Consistency is key to programming style
- C truncates the results of integer division (so 5/9 would be 0). To avoid this, use floats (5.0/9.0 for example).
  - See [temps.c](./examples/temps.c) for a temperature converter using ints and [floatTemps.c](./examples/floatTemps.c) for a temperature converter using floats.
- See ch 7 for `printf`. Briefly: `printf` takes a string of chars to be printed and any number of arguments to replace the `%` constructions. 
- `printf` is imported from `stdio.h`
- The input method `scanf` is also covered in ch7

- You can define the field size of the `%` constructions by adding a number after the `%` like `%3d` for a field at least 3 digits wide.
  - For floats, you must specify the entire width and the width after the dot. For example, `%6.1f` gives at least 6 spaces for the entire number and 1 space for the fractional part (aka mantissa) leaving at least 5 spaces for the whole part (aka characteristic).

- You should use decimal points when declaring floats even if they only have 0s in the fractional part.
- printf also recognizes
  - `%o` for octal
  - `%x` for hexadecimal
  - `%c` for character
  - `%s` for string
  - `%%` for % itself

# 1.3 The For Statement

- See [forTemps.c](./examples/forTemps.c) for an example of for loops.
- The syntax is similar to java

# 1.4 Symbolic Constants

- The `#define` keyword defines a *symbolic constant* (aka *symbolic constant*) to be a set of characters
- See [constantTemps.c](./examples/constantTemps.c) for an example
- Notice, *symbolic constant* lines don't require a semicolon at the end.

# 1.5 Character Input and Output

- __Text stream__: a sequence of characters divided into lines; each consisting of zero or more characters followed by a newline.
- Use `getchar` to read a single character and `putchar(c)` to write a single character.
- See ch7 for input from files.

## 1.5.1 File Copying

- 