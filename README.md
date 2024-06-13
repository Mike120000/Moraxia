# Moraxia
A programming language I'm working on :p

# Syntax
## Comment
Comments are segments ignored by the compiler.

**Example:**
* \`This is a comment\`

## Assignment
Variables and constants are paces in the CPU used to store certain values.

**Examples:**
* Variable: x = 5;
* Costant: cst x = 5;

## Function declaration
A function is a part of the code that performs instructions on several arguments and returns a value.
*Return-lines* are the instructions that get returned, they don't contain a ';' at their end.
A function can contain multiple return-lines through conditionals(e.g. if, else, ...), but once the code reaches a return-line, it exits the function.

**Example:**
* func add(a, b) { a + b }

## Function calling
You can access the instructions inside a function using certain arguments by calling said function.

**Example:**
Consider f to be an already-defined function that takes two arguments. Here, we'll store the returned value in a variable called 'x'
* x = f(5, 3);

## Operators
An operator is a symbol that denotes an operation. There are mainly two types:
### Built-in
Pre-defined operators in the syntax.

**Examples:**
* 5 + 2
* 8 - 7
* 6 * 4
* 9 / 3

### Custom operators
Operators that the user defines.

**Example:**
Consider f to be an already-defined function that takes two arguments. The *def* keyword acts as a function with instructions and return-lines.
* def a # b { f(a, b) }
