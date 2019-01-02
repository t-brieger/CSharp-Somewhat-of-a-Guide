# Naming

## Variables

###Class- and Namespace-Scope (Classes, Fields, Members, Functions and Methods)
In C#, following the naming conventions, classes, fields, members, Functions and Methods usually start with a capital letter and then have every other word appended without spaces, but again starting with a capital letter (this is commonly called Upper Camel Case). An example name would be `CoolBookAboutCSharp`

###Method-Scope
Variables in Method-Scope usually follow the same naming convention as in Class- and Namespace-Scope, but they start with a lowercase letter (usually called camel Case). An example name for this would be `coolBookAboutCSharp`

###Exception: unused variables
variables that are never used and just required to call a method (for example unused `out` parameters) or iterate over something are sometimes named `_` (one underscore). if that name is already used, then it's instead two underscores, if that's used, 3 underscores, etc.

###Constants
Constants are, depending on the coder, either in all-Uppercase or follow the same naming convention as the rest of the scope they're in.

###Enums
Enums themselves follow the naming conventions of classes, and the members inside them are either all-uppercase or in upper-camel-case as well

##Indentation
The standard is to indent by 4 spaces for every block (**not** tabs). For example:
```cs
class a
{
    public void b(int c, int d)
    {
        if (0 != 1)
        {
            DoSomething();
        }
    }
}
```

##Syntactic Constructs

###Curly Braces and Conditionals
While this may be the most debated of the naming conventions, the current standard in C# is to place opening and closing Curly Braces on a new line and `else`s on the same line as the closing Curly bracket of the corresponding`if`, without a space. For example:
```cs
if (x == y)
{
	DoSomething();
}else
{
	DoSomethingElse();
}
```