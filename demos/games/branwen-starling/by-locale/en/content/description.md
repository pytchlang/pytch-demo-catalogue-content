# Branwen and the Starling: A Welsh Tale

Here’s the short version:

Branwen, Bendigeidfran’s sister, had married Matholwch, the King of
Ireland.

This angered Efnysien, Branwen’s other brother, as his permission was
not asked, so he killed all of Matholwch’s horses.

Branwen and Matholwch managed to escape to Ireland, but because of the
actions of Efnysien, Matholwch decided to imprison Branwen.

In jail, Branwen reared a Starling to fly home to Wales carrying a
letter for Bendigeidfran.

You can find a longer version of the legend of Branwen on the
[Wikipedia page](https://en.wikipedia.org/wiki/Branwen).


# Playing the game

Start the game with the green play button.  After the starting
message, you start controlling the starling.  It will start falling,
but you can use the “a” key to fly upwards.  Don’t fall into the sea
or get caught by the ospreys!


# How the code works

A few points about the code:

* There are various _green flag_ scripts, but the start of the game
  itself is handled by a `"start-game"` message.

* The continually scrolling background is implemented by the
  `Background` sprite.  It moves gradually leftwards until it’s time
  to jump back to its starting position.

* The `Starling` has *two* _when green flag clicked_ scripts, because
  there are two loops which need to run at the same time.  You _could_
  write this as one script but it would be quite fiddly.

* The `Osprey` sprite picks a random height, and goes to the far right
  of the screen at that height.  It then moves leftwards across the
  screen, and when it reaches the edge, starts the whole process
  again.

* The code uses `self.stop_all()` as a way to make all the different
  scripts finish when the player either wins or loses.
