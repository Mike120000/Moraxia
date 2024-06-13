# Moraxia
A programming language I'm working on :p

# Syntax
## Data types
Moraxia allows you to specify the data type or not. In case you don't, it detects it by itself.

**Examples:**
* int x;
* x = 5;

## Operators
Moraxia has a wide range of built-in operators and allows you to create custom ones(if they don't already exist).

### Built-in
* Basic arithmetic operators:
  * addition: a + b
  * subtraction: a - b
  * multiplication: a * b
  * division: a / b
  * negation: -a
* Additional arithmetic operators:
  * modulo: a % b
  * integer division: a // b
  * exponentiation: a ^ b
* Logical operators:
  * AND: a && b
  * OR: a || b
  * NOT: !a
  * XOR: a ^ b
* Comparative operators:
  * Equal to exactly: a === b
  * Equal to 1% error: a == b
  * Not equal to: a != b
  * Approximately:
    * Approximation in Moraxia is a little complicated. But to put it in simple terms, there are levels of it:
    * 10% error or less: a ~ b
    * 5% error or less: a ~= b
    * 3% error or less: a ~~= b
    * Custom approximation: approx(a, b, error_rate)
  * Greater than strictly: a > b
  * Greater than or equal: a >= b
  * Less than strictly: a < b
  * Less than or equal: a <= b
* Iterator-object operators:
  * Index: itr\[i\]
* Pointers:
  * Point to: *p
  * Address of: &p
  * Dereference: *p
* Iterator:
  * The iterator operator does what the name suggests, it iterates:
  * <iterable> is short for: "for element in iterable".
  * This operator can be used in functions:
  * Consider f to be a pre-defined function: f(<iterator>) is equivalent to: "for element in iterator { f(element); }
  * This operator has some built-in functions and names to help with storing it, and naming its variables:
    * args: This refers to the arguments of a function
    * name(): This function sets the name of the element as the name of a variable.
      * Usage(inside a class): func f(self, ...) { self.name(<args>) = <args>; }
      * The code snippet you saw does what you probably have guessed, it assigns each argument to its value.
      * Example: "func f(self, width, height) { self.name(<args>) = <args>; }" is equivalent to: 

## Custom
Defining custom operators is a simple process:
def 
## Comments
Comments are segments ignored by the compiler.

**Example:**
* \` This is a comment \`

## Assignment
Variables and constants are paces in the CPU used to store certain values.

**Examples:**
* Variable: let x = 5;
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
