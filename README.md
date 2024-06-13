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
* Pointer operators:
  * Point to: *p
  * Address of: &p
  * Dereference: *p
* Iterator operator:
  * The iterator operator does what the name suggests, it iterates:
  * <iterable> is short for: "for element in iterable".
  * This operator can be used in functions:
  * Consider f to be a pre-defined function: f(<iterator>) is equivalent to: "for element in iterator { f(element); }
  * This operator has some built-in functions and names to simplify interacting with it:
    * args: This refers to the arguments of a function
    * name(): This function sets the name of the element as the name of a variable.
      * Usage(inside a class): func f(self, ...) { self.name(<args>) = <args>; }
      * The code snippet you saw does what you probably have guessed, it assigns each argument to its value.
      * Example: "func f(self, width, height) { self.name(<args>) = <args>; }" is equivalent to: "func f(self, width, height) { self.width = width; self.height = height; }"
* Class access operator:
  * This operator is used to access the initial values of a class as well as the functions inside it.
  * Usage: 'self.x', 'self.f(8, 2)', 'MyClass.p', ...

### Custom
Defining custom operators is a simple process:
* Assume the custom operator is '#', it takes two integers and returns f(a, b)—an already-defined function.
def int a # int b { f(a, b) }

**Note:** The 'def' keyword is similar to a function, it can have multiple instructions and a return-line.

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
To access the instructions and return value inside a function f with specified arguments, you can call it.

**Example:**
Consider f to be an already-defined function that takes two arguments. Here, we'll store the returned value in a variable called 'x'
* x = f(5, 3);

## Structures
A structure is a bunch of variables/constants in one place.

**Example:**
struct MyStruct {
 int value;
 char* name;
}

## Enumerations
An enumeration is a bunch of values stored together, each one represents a positive integer starting from 0.

**Example:**
enum Message { Succes, Failed };

**Usage:**
struct Connection {
 Message success_state;
 int error_code;
}

## Classes
A class is a structure bound with certain functions.
The structure serves as an initialization of values for the class.
To access the values in the structure of a class, or the functions of said class, you can use 'self' followed by the "class access operator" and then the name of what you need to access(e.g. self.x, self.f(5, 3), ...)

**Example:**
* Consider the structure 'MyClass' to be already defined, containing: 'int x', and 'int y'.
class MyClass {
 func f(self) {
  self.x + self.y
 }
}
