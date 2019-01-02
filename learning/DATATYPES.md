# Data Types

## What is a Data Type?

A data type is, as the name suggests, a type of data. Giving each type of data its own definition enables them to function differently from each other.

In C#, there are a few so-called "primitive" data types - Data types which you can create using a literal. (a literal is a way of representing data by just typing it in your source code instead of calling a function to get it.)

## Boolean
A boolean is the simplest form of data, only being able to represent two states; on and off. (in binary, this is represented as 1 and 0.)

To create a boolean, simply use the literal `true` for a value of 1 or on and `false` for a value of 0 or off.

```cs
boolean positive = true;
boolean negative = false;
```

## Integer
An integer is the type of a whole number.

In C#, there are a few different types of Integers: `byte`, `short`, `int` and `long`. (there are also signed/unsigned variants of them, but if you're at the point where you may need them, you'll probably know what they are already, so for keeping it short, they are not included here.)
The difference is in the range of values they can store: byte goes from 0 to 255,
short goes from -32768 to 32767,
int goes from -2147483648 to 2147483647 and
long goes from -9223372036854775808 to 9223372036854775807.

To use them, simply type a number literal:

```cs
int negFive = -5;
short maximumValue = 32767;
```

## Floating point numbers
Floating point numbers are like integers, except they can store fractional digits too!

again, C# has 2 types of them: `float` and `double`. `double` has a higher range and is more precise, but also takes up more space in Memory.

To create them, either type a number literal followed by a dot (`.`) and then another number or a number literal followed by the letter `d` for doubles or `f` for floats.

```cs
float oneThird = 1.0 / 3f; //this is about 0.3333334, because as mentioned, they do not have infinite accuracy.
double oneThirdDouble = 1d / 3d; //this has some more 3s, but still ends in a 4 for the same reason
```

## Character
A `char` is any character you can type (and some more). To create `char`s, you surround a single character with single quotes (`'`) OR type a backslash and then any of the following:
* another backslash for a character representing a backslash,
* a `n` for a newline (that's a character too!),
* an `r` for a carriage return (don't worry if you don't know what that is, it dates back to typewriter times.),
* an `a` for an ascii alert character (if you send that to the output, you may hear some sound played over your speakers) or
* another single quote for a single-quote character. (if you didn't type the backslash here, the compiler would think that you're creating an empty char.)

```cs
char a = 'a';
char space = ' ';
char singleQuote = '\'';
char alert = '\a';
```

## String
A string is the type used for sequences of characters

To create a string, encapsulate text within quotation marks (`"`).

You can use all the same "escape sequences" (those starting with a backslash) in a string that you can use in a char and one more: `\"` to indicate that you don't want to end the string but rather have a quotation mark appear inside of it.

```cs
String helloWorld = "Hello, World!";
String quotation  = "\"Hello\", I said";
String lineSeperated = "Hello\nWorld";
```

## Array

(write something about arrays)