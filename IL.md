#What is .NET?
.NET is a language family that includes C# (obviously, since it's explained here), Visual Basic, F# and Visual C++.

Its main difference to other Compiled languages is that it's a lot more portable: with most other languages, you'd have to provide the end user with seperate binary files for each platform.

With .NET, however, You only have to compile your source code once and then get a file with "IL" (Intermediate Language) code inside it.

This code is a lot like native bytecode, in that it contains non-human-readable instructions, but it can't be executed by the computer without the need for an extra program either.

#### so, what is this good for if it can't be used by the computer?
the IL code is already optimized by the compiler and is already "broken down" into instructions (from the high-level syntactic constructs of the language).

When you run IL code, your computer translates the instructions in the IL code to those instructions that it can execute natively using a special program: the .NET runtime.

#### why is this better than other approaches?
there are 2 (major) other approaches to compiling a program: compiling the program to native code directly or interpreting it without a real compilation step.

The advantage over compiling to native code directly is that for every target architecture (for different operating systems and processors), you would have to provide a seperate binary, while with .NET, you can simply distribute a single IL file and then let the .NET runtime do the architecture-specific work for you.

This approach does have a disadvantage when compared to compiling to native code as well though: Performance. The reason for that is that instead of simply passing the File to the processor as-is, IL files have to be "translated" first, which, of course, takes some amount of processing power.

(add pro & contra for interpreted langs)