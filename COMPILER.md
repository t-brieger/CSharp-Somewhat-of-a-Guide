#The Compiler

##What is the Compiler?
by definition, it's a piece of software that transforms some format into another one.

The Compiler we're working with here mostly is one that transforms our C# Code into Machine-Readable Code (Assembly). It also shortens your code a lot (optimizes it), so this:
```
set a to 0
add 1 to a
subtract 1 from a
set a to 42
output a
```
would become
```
output 42
```
(note: neither of the examples are real C# code, but since this is likely the first page you encounter, I decided to make it readable for non-coders as well.)