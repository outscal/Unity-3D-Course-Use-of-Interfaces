## Use of Interfaces

Interfaces are useful when you want to refer to several disparate objects by a common attribute - this makes it possible to put things into lists and iterate through them, even if they are very different classes. 

For example, a Robot and a Crate are very different objects in a game, but if both implement a Breakable interface, they can be considered equal objects, at least in the respect that they are both breakable.
