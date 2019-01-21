# saga2-ds-meat-chainer
A Prolog program that tells you how to get certain monsters in the DS remake of SaGa 2.

So far, it has two predicates:
meat(Eater,Meat,Result), and meatchain(Eater,Result,Meatchain).

All you have to do is compile the .pl file in a garden-variety Prolog compiler (like SWI or gprolog), and type something like:
  meatchain(minidragon,sprite,How).
  
And it will provide you with a series of lists of meats to eat that will turn your minidragon into a sprite.
If you don't want to use a certain meat (let's say jaguar or skeleton), you can type:
  meatchain(minidragon,sprite,How), +\member(jaguar,How), +\member(skeleton, How).
  
Or, in other words, "What species of monster meat must my mini dragon eat (and in what order), to become a sprite, if I don't want to eat jaguar or skeleton"?

You can also type things like,
  meat(minidragon,Meat,Result).
"What can my minidragon eat, and what will it become?"

Or
  meat(slime,Meat,zombie).
"Is it possible for my slime to eat something that turns it into a zombie?"

Prolog is an amazing language for things like this. Did you know it's older than the home computer, and people still use it today? Eat it, C.


# TO DO

* Finish adding all the transformation rules
* Find out the English fan-translation names for everything
* Add a boolean thingy so I can divide all the meats by the worlds they are found in
* Add another predicate that finds the latest monster in Meatchain that has index of 3n - x - 1, where x is the number of meats you have already eaten mod 3, and n is a natural number. (As near as I can figure out, that's the one you inherit some monster power from. Wouldn't it be cool if this program calculated how to get you a fairy that had a sword's immunity to element damage?)


# Contributors welcome!
I like this game, and programming this is a fun little challenge. Whoever wants to join is welcome.
