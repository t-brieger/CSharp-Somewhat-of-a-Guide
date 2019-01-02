#The Compiler

##What is a Compiler?
By definition, a compiler is a piece of software that transforms some format (mostly code) into another one (executable files).

The one we mean here when we say `[the] compiler` is one that transforms our C# Code into IL code \([what is IL code?](IL.md)\).

##What else does the compiler do?
Before transforming it into IL, the compiler also makes your code run faster. To do this, it removes statements that are useless.&#10;&#13;
For example, this "code" (this is not C#, it's a made up language that closely resembles english to make it easier to understand):
```
set a to 0
add 1 to a
subtract 1 from a
set a to 42
output a
```
would become this:
```
output 42
```

Another very important thing that the compiler does is tell us where we wrote invalid code, for example, following the format of the "code" above:
```
ouptut 42
```
in this piece of code, the compiler would tell us that it does not know what `ouptut` means and sometimes even give us suggestions on what we may have meant (in this case, `output`).