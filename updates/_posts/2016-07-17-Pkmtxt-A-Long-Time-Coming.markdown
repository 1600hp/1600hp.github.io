---
layout: post
title:  "Pkmtxt: A Long Time Coming"
date:   2016-07-17 11:59:59 -0400
categories: updates
excerpt: A touch of nostalgia, a bit of philosophy, and way too much code.
tags: "pokemon programming python"
published: true
---

I'm starting on one of the more ambitious pieces of non-school-related code I've ever worked on.  I'll be making a Pokémon text adventure.  This may seem like a kind of arbitrary combination of things, but there's a fair bit of motivation behind it.  Let's walk through it.

Pokémon Go was disappointing to me.  Sue me.  In its current form, it doesn't really do anything that I want from a Pokémon game.  This may change eventually as the game sees continued development, and I'm certainly not writing it off yet, but at the moment I'm just not into it.  I love the Pokémon franchise, though, and I'd like to do more with it.

I had to get good at Python this summer.  As a LabVIEW programmer first and foremost, I was never quite at peace with it.  This is mostly due to the dynamic typing inherent to the language.  Now, more than halfway through my internship, I no longer actively dislike it.  I do want to see what it's like to develop large-scale code with it, however.  Previously, I've used Python for small scripts, wrappers, and other minor applications.  How does it stand up to more complex requirements?

For some reason, causal determinism just keeps coming up in conversation for me.  That phrase probably isn't familiar to many people, and I won't be going into it in this post.  Suffice it to say, it's a mental model that has shaped a lot of my how I see the world.  What does this have to do with anything?  Well, in its most basic form, a text adventure exemplifies a causally deterministic world.  So here we are.  I'm writing a deterministic Pokémon game in Python.  See how that works out?

Now, like I said, this is pretty ambitious.  I'll have to design a passable emulation of Pokémon's battle system, a functional natural language interpreter, and define approximately a shit-ton of ways of interacting with the world, all while maintaining my code in such a way that it remains easily extensible and understandable.  Odds are, I won't finish this project.  Still, it'll be fun while it lasts.  I'll be posting my progress occasionally here, both to organize my thoughts, and to keep myself motivated.  With that, take a gander at the main file of Pkmtxt.

{% highlight python %}
from world import World
from interface import Interface
from interpreter import Interpreter

class ClockworkUniverse():
  def __init__(self):
    self.universe = World()
    
  def tick(self, cmd):
    self.universe = cmd(self.universe)
    
if __name__ == "__main__":
  universe = ClockworkUniverse()
  while True:
    sentence = Interface.get_sentence()
    cmd = Interpreter.interpret(cmd, universe)
    universe.tick(cmd)
{% endhighlight %}

Well that's certainly straightforward, huh?  In english:

* Define a universe
* Retrieve input from the user
* Translate that input into a function 
* Enact that function upon the world, modifying it in some way

Safe to say this will change to some extent during development, but the overall shape will remain the same, and provides a good picture of what any given iteration looks like on the high level.

Stay tuned.  It's about to get interesting.