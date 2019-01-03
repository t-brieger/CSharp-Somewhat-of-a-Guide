# Functions

## What is a Function?

A function is a command that can be used to performa one or multiple actions. They can contain however many lines of code you would like, and can be used however many times by just calling them.

### Why Should I Use Functions?

Using functions will decrease the the amount of coding needed.

If you want to run multiple lines of code multiple times, then putting that code into a function will reduce the lines needed to 1 - the function call. It also means that you can update the code you want to run, easily, rather than having to change a line in each duplicate section of code.

## Arguments

### What is an Argument?

An argument is something that can be passed into a function to then be used inside of the function.

```cs
void Greet(String name)
{
    Console.WriteLine("Hello, " + name + "!");
}
```

```cs
void GreetLong(String firstName, String lastName)
{
    Console.WriteLine("Hello, " + firstName + " " + lastName + "!");
}
```

### Default Value

By default, the values of arguments are all null, and so every one must have a value passed to it. However, you might want to give default values for arguments. This can be done by adding an equals sign and then the value, just like you were creating a variable.

```cs
void Greet(String name="John")
{
    Console.WriteLine("hello, " + name + "!");
}
```

if this function was called without specifying parameters, `hello, John!` would be outputted.

### Passing Arguments

To pass values to function arguments, you will need to add the data to the set of parentheses.

```cs
Greet("Bob");
```

If there are multiple arguments for a function, to set their values, you will need to set them in the order they come in the function.

You can also pass the name of the argument and then it's value.

```cs
Greet(name: "Bob");
```

Passing them with the name means that you can give the values anywhere in the parentheses.

```cs
GreetLong(LastName: "Guy", FirstName: "Just Some");
```

These aren't an either/or situation, though. Both can be used together.

```cs
GreetLong("Some", second_name="Guy");
```

However, you can't pass a named argument and then an unnamed one, as the order of the arguments does matter.

```cs
GreetLong(second_name="Name", "Random");
```

Using the name of the argument will improve readability of the code, and if you think someone else will need to understand what the arguments mean, it might be a good idea to use them.

### What are `params`

When making a function, you can specify that in the arguments, it can accept either only a single argument with `params` or a number of arguments and then one with `params`. What `params` means, is a limitless amount of arguments, so creating a function that accepts it, means that all arguments provided to the call after specific ones, will be placed in an Array. You can then access the arguments under the name you gave the parameter in the function to use them.

```cs
void Function(params String[] args)
{
    foreach (String item in args)
    {
        Console.WriteLine(item);
    }
}
```

```cs
Function("Hello", "World!", "I", "Can pass", "h", "o", "wev", "er", "many" "arguments I want to.");
```

##  Returning Information

Functions can return information to be used elsewhere. to do this, you have to specify the return type in front of the function name instead of `void` and then return from anywhere withing the function using the `return` keyword.

After return, the execution of the function stops, so that this example:

```cs
int Sum(num1, num2)
{
    return num1 + num2;
    Console.WriteLine("hi");
}
```

```cs
Console.WriteLine(Sum(1, 2));
```

never writes `hi` to the console.

## Annotations

### What is an Annotation?

