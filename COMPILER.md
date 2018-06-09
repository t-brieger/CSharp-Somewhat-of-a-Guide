#The Compiler

##What is the Compiler?
technically, it's a piece of software that transforms some format into another one.
The Compiler we're working with here mostly is one that transforms our C# Code into Machine-Readable Code (Assembly). It also shortens your code a lot (optimizes it), so this:
```cs
int a = 0;
a++;
a--;
a = sqrt(a) * sqrt(a)
Console.WriteLine(a)
```
becomes this:

```cs
Console.WriteLine(0)
```