
#What is .NET?
.NET (pronounced dot net) is a family of programming languages which includes C# (which we'll be explaining here), Visual Basic, F# and Visual C++.

Its main difference to other frameworks or families is that it's a lot more portable: with most other languages, you have to provide the end user with seperate binary (executable) files for each platform.

With .NET, however, You only have to compile your source code once and then get a file with "IL" (Intermediate Language) code inside it.

This code is a lot like native bytecode, in that it contains non-human-readable instructions, but it can't be executed by the computer without the need for an extra program either.

#### so, what is this good for if it can't be used by the computer?
the IL code is already optimized by the compiler and is already "broken down" into instructions (from the high-level syntactic constructs of the language).

When you run IL code, your computer translates the instructions in the IL code into those instructions that it can execute natively using a special program: the .NET runtime.

#### why is this better than other approaches?
there are 2 (major) other approaches to compiling a program: compiling the program to native code directly (as seen in, for example, C++ or Rust) or interpreting it without a real compilation step (like python, ruby or javascript).

The advantage over compiling to native code directly is that for every target architecture (for different operating systems and processors), you would have to provide a seperate binary, while with .NET, you can simply distribute a single IL file and then let the .NET runtime do the architecture-specific work for you.

This approach does have a disadvantage when compared to compiling to native code as well though: Performance. The reason for that is that instead of simply passing the File to the processor as-is, IL files have to be "translated" first, which, of course, takes some amount of processing power.

(add pro & contra for interpreted langs)

<quiz>
    <question>
        <p>Which of those languages usually runs faster?</p>
        <answer correct>C++</answer>
        <answer>C#</answer>
        <answer>Python</answer>
    </question>
</quiz>