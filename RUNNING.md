#How to run your code
##By Compiling it with csc.exe
first, make sure you have installed the .NET framework ([this one](INSTALLATION.md))
after that, you can either compile it from within an IDE (often by clicking a button or hitting f5 on the keyboard) or, if you're not using one, run `<Your .NET Install Directory>\csc.exe /out:<Output File> <Input File>` where Output File is the .exe or .dll you want to save your compiled code as and Input File is your .cs, .sln or .csproj file that you want to be compiled. You **can** leave out the `/out:blablabla` part.

after that, just start the file if it's an exe or use it in another project if it's a dll.

##By Compiling it online
There are a multitude of webapps that allow you to compile C# code online and even run it in your browser. those, of course, can not replace a proper IDE / runnable file when it comes to things like creating windows or doing complex math-y equations, but they are a quick alternative if you don't want to boot up your IDE just for a small project.

a few examples of this are [rextester](http://rextester.com/), [dotnetfiddle](https://dotnetfiddle.net/) and [csharppad](https://csharppad.com/)