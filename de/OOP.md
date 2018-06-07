#Object-oriented Programming (OOP)

Object-orientation is a kind of programming based on "objects"

###What are Objects?
Objects can be imagined as blueprints. for example, let's say you have a Human object. it has "fields", meaning properties that can be accessed from the outside, for example hair color and gender (gender may not be the most fitting example, since you can generally change most fields) and it has "methods", which do things relative to the human that's doing them. Examples for methods are Breath, walk.
Let's examine the Breath-example-function a little closer:
if you haven't read the [Methods](METHODS.md) section, here's the short version:
methods take in parameters (Sometimes) and "give back" a value (often, but not always).

Breath, for example could take in a number that specifies the length of the breath and give back a boolean that indicates whether it could execute (if the human could breathe). That value may then be used to give it to the Brain to, for example, indicate that the Human should stop diving now.
The Main thing that would happen in the method would be setting the "Airamount" Field to (Whatever the Lung capacity is)

The great part about Objects is that they can be used infinetely in other classes / objects. This means that we could now have a world class that just contains ~7,500,000,000 "Human" Objects.

#THIS NEEDS TO BE CONTINUED