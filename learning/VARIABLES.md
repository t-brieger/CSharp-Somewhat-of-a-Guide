# Variables

## What is a Variable?

A variable is essentially a label for a value. They contain a piece of data. A variable can contain any [data type](DATATYPES.md). However, once the type has been set, it cannot be changed anymore.

## Why Should I Use Variables?

Variables help improve readability of code, and can reduce the amount of coding needed.

Say that you need to use a string again and again, you could just write the string each time, but then if you wanted to change the string, you would need to change each mention of the string. Instead, you can use a variable that contains the string. Meaning that if you wanted to change the string, you would only need to change it once.

## Using Variables

To use a variable, the variable must first be defined. After that, it may be referenced or changed.

### Defining Variables

To define a variable, you simply write A type, followed by the desired name followed by an equals sign and then the value the variable will have. This may be the result of a function call or a literal.

```cs
String MyVariable = "A simple string";
```

Now, the variable, "MyVariable" may be used in the code.

### Changing Variables

Changing a variable is a lot like defining it, the only difference is that the type is not specified again:

```cs
String MyVariable = "A simple string";
MyVariable = "A different string";
```

The first line will create the variable and specify that it's of type `String` and give it a value of `A simple string`, and the second line will change the value of the variable to `A different string`.

### Referencing Variables

To reference a variable, you simply write the name of it where you would like it to be used.

```cs
MyVariable = "A simple string";
Console.WriteLine(MyVariable);
```

This will print `A simple string` to the standard output (usually the terminal).

