# saga2-ds-meat-chainer
A Prolog program that tells you how to get certain monsters in the DS remake of SaGa 2.

So far, it has two predicates:
meat(Eater,Meat,Result), and meatchain(Eater,Result,Meatchain).

All you have to do is compile the .pl file in a garden-variety Prolog compiler (like SWI or gprolog), and type something like:
  meatchain(minidragon,sprite,How).
  
And it will provide you with a series of lists of meats to eat that will turn your minidragon into a sprite.
If you don't want to use a certain meat (let's say jaguar or skeleton), you can type:
  meatchain(minidragon,sprite,How), +\member(jaguar,How), +\member(skeleton, How).
  
Or, in other words, "


# TO DO

* Finish adding all the transformation rules
* Find out the English fan-translation names for everything
* Add a boolean thingy so I can divide all the meats by world
