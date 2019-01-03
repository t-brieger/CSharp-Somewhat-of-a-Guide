# Namespaces

A Namespace is a collection of Classes for you to use, usually written by someone else or included with C#, though you are able to easily write your own Namespaces and distribute them for others to download and use.

## Importing Namespaces

A Namespace can be imported with the using statement.

```cs
using System;
```

This will import the "System" namespace, which includes all kinds of classes, including `Console`, which makes it possible to take input from the user and output to the terminal.

```cs
Console.WriteLine("this string will appear on your terminal");
```

This will then print "this string will appear on your terminal".

Though if you need to use this function multiple times, and don't want to type out the Class name each time, you can import everything from the Class into the local namespace, like so:

```cs
using static System.Console
```

and then use it like this:

```cs
WriteLine("this string will appear on your terminal");
```

however, `using static` is generally considered bad practice because it causes problems when 2 or more of the classes you imported this way have a similarly named method.

## Creating namespaces

To create namespaces, simply start a block using `namespace <name>`, where name is the name you want to give the namespace.

```cs
namespace SomeNamespace 
{
    public class ABC
    {

    }
}
```

namespaces can **not** directly contain Variables or methods, they can only contain classes (which, themselves, *can* contain them.)