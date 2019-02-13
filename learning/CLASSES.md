# Classes

## What is a Class?

A class is an object that can contain variables and methods. Multiple instances of the class can be created and used independent of eachother (except when the class is marked as static).

At the most basic level, a class is just a way to bundle a bunch of data into one variable.

### Why Should I Use Classes?

Classes are a core principle of object-oriented languages like C#, and play a key role in reducing the amount of reused code. Often, you'll find that you need to think of a piece of code like an object, and when coming across a problem like this, you'll most likely want to use an object. For instance, say you're writing a game with a quest system, you'll probably want to make a quest manager object, with methods to add, create and remove quests, and then have a quest class, with methods to update, find info about, and complete the quest, which each quest will subclass.

## Using Classes

### How to Create a Class

The code below will create an empty class.

```cs
class EmptyClass
{
}
```

## Inheritance

### What is Inheritance?

Inheritance is when a class extends another, or multiple others.

When a class is extended by another, the new class will contain everything the extended class had and can (but does not have to) add more things to itself

### How to Inherit From a Class

To inherit from another class (extend it), simply type it's name after a colon:

```cs
class MyClass : ClassToInheritFrom 
{
}
```

You can also implement interfaces, which is very similar to extending classes:

```cs
class MyClass : IMyInterface //by the naming conventions, Interfaces start with a capital I.
{
}
```

unlike interfaces, however, You can only extend 1 class, so this:

```cs
class MyClass : OtherClassOne, OtherClassTwo
{
}
```

Is invalid while this:

```cs
class MyClass : OtherClassOne, IMyInterfaceOne, IMyInterfaceTwo, IMyInterfaceThree
{
}
```

is not.

Note though that when you implement Interfaces, you have to re-define methods that are defined in them.

If no class is given to inherit, the class will inherit from `Object`. This also means that every class "indirectly extends" Object.

## Constructors

### What is the Constructor?

The Constructor is a method that is run whenever an instance of the class is created using the `new` keyword. It is where many of the initialization happens.

```cs
class MyClass 
{
    String str;
    int fortyTwo;
    public MyClass(String a) //A constructor must have the same name as the class it is in and not have a return type.
    {
        str = a;
        fortyTwo = 42;
    }
}
```

if no Constructor is specified, a default one will be created: 

```cs
class MyClass 
{
}
```

Is equivalent to

```cs
class MyClass
{
    public MyClass()
    {
    }
}
```

### Running the Constructor of an Extended Class

If you extend from a class that sets variables in it's Constructor, you will notice that those variables will not be set in your extended class if you have a Constructor. This is because the extended class's Constructor is never run. To fix this, you will need to call `base` using this special syntax:

```cs
class MyClass : OtherClass
{
    public MyClass() : base() //base(arguments) runs the base classes (the class you're extending from) constructor with the specified arguments.
    {
    }
}
```

## Methods {#methods}

### What is a Method?

A method is what functions that belong to an instance of a class are called. They are the same as normal functions, except they are part of the instance, instead of the class.

### How to Create a Method

```cs
public void MyMethod() //do not use the static keyword when defining methods.
{
}
```

## Static things

### What does static mean?

A static variable or method is one that belongs to the class. In every instance of the class, class variables will always stay the same. They are defined using the `static` keyword before the type.

### How to create a static variable or method

```cs
class MyClass
{
    public static string NameOfThisClass = "MyClass";
}
```

### How to access static variables or methods

In the example above, where `MyClass` has a static String `NameOfThisClass`, you could access it using: 

```cs
MyClass.NameOfThisClass
```

## Instance (non-static) Variables and methods

### What is an Instance Variable or method?

An instance variable Or method is a variable or method of the class that can be used from an instance. They are defined without the `static` keyword.

### How to create them?

```cs
class MyClass
{
    string MyName = "Bob";
}
```

## Instances

### What is an Instance?

An instance of a class contains everything that the class has. The instance can use the non-static methods and variables, and can even change what's stored in those variables.

### How to Create an Instance

To create an instance, you simply type the `new` keyword, followed by the classes name followed by the arguments that the parameter takes in parentheses.

```cs
class MyClass
{
    string bla2;
    public MyClass(string bla)
    {
        bla2 = bla;
    }
}
//to create an instance of the above class, you would do:
MyClass mc = new MyClass("Random String"); //Don't forget to specify the type of the class before the variable name.
```

## Example

```cs
class QuestManager
{
    List<Quest> Quests;
    public int active;
    public QuestManager()
    {
        Quests = new List<Quest>();
        active = 0;
    }

    public void Start(Quest quest)
    {
        Console.WriteLine("started quest: " + quest.Name);
        
        quest.Start();
        Quests.Add(quest);
    }
        
    public void Complete(Quest quest)
    {
        quest.Complete();
    }

    public void Ditch(Quest quest)
    {
        Console.WriteLine("Ditched: " + quest.Name);
        
        quest.Ditch();
        Quests.Remove(quest);
    }

    public void DitchCurrent()
    {
        Ditch(GetActiveQuest());
    }

    public void CompleteCurrentQuest()
    {
        Complete(GetActiveQuest());
    }

    private Quest GetActive()
    {
        return Quests[active];
    }
}
```

```cs
class Quest
{
    public string name, description;
    public Quest(string name, string description)
    {
        this.name = name;
        this.description = description;
    }

    public void Start()
    {
    }
        
    public void Complete()
    {
    }

    public void Ditch()
    {
    }
}
```

```cs
QuestManager manager = new QuestManager();
Quest fetch_sword = new Quest("Fetch Sword", "Delve into a dungeon and retrieve a sword.");
manager.Start(fetch_sword);
```

