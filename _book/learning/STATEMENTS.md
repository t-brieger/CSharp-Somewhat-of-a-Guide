# Statements

## What is a Statement?

### Why Should I Use Statements?

## Simple Statements

## Compound Statements

### If Statements

The `if` statement can be used to check if an expression is true or false.

This if statement, for example, checks the equality of 0 against 0.

```cs
if (0 == 0)
{
    Console.WriteLine("0 is equal to 0.");
}
```

Will always be true and because of this, it will always print, "0 is equal to 0."

#### Else

If you want to run some code when the argument is false, you can use `else`.

```cs
if 0 == 1
{
    Console.WriteLine("0 is equal to 1.");
}else
{
    Console.WriteLine("0 is not equal to 1.");
}
```

#### In-Line (Ternary operator)

The if statement can be used in-line, to set a value to a piece of data depending on if the condition evaluates to true or false.

The syntax for this is `condition ? (Value when condition is true) : (Value when condition is false)`. This form of the if statement can **not** be used to execute statements, it always has to only be Expressions.

```cs
Console.WriteLine(0 == 0 ? "0 is equal to 0" : "0 is not equal to 0");
```

### Loops

#### While Statement

The while statement will continue to run the code it contains until the expression it was given is not true.

```cs
while (0 == 0)
{
    Console.WriteLine("Hello");
}
```

This will print `Hello` until the program is closed, since 0 always equal to 0 and thus the program never stops.

If you want your program to loop forever, it is best to use `while(true)`, as it is better in terms of readability and does the same thing as the while statement above, since `true` is always `true`.

#### For

(bla.)