# Launch one thing at a time

Pressing the left arrow key makes the pink cloud (on the left) drop a
raindrop.  Only one raindrop can exist at a time.

## The `LeftCloud` sprite

The script for the cloud isn't very important for this example.  The
cloud sets itself to have a sensible size, then glides left and right
across the left-hand half at the top of the screen.

## The `LeftRaindrop` sprite

The important idea here is that the raindrop needs to keep track of
whether it is falling.  To do this, we give it a variable `falling`
which can be either `True` or `False`.

When the game starts, the drop is not falling, so the _green flag_
script records this fact by setting `self.falling` to `False`.  That
script also makes the raindrop a sensible size and hides it.

When the left arrow key is pressed, the script first checks whether
the drop is already falling, and if so, uses the `return` statement to
stop running the script immediately.  If the drop is _not_ currently
falling, we want to start it falling, so set the variable to say that
it now _is_ falling.  The raindrop then goes to just below where its
cloud is, and moves down the screen.  When it has gone off the bottom,
it records the fact that it's no longer falling.


# Launch many things at a time

## The `RightCloud` sprite

The script for the cloud isn't very important for this example.  The
cloud sets itself to have a sensible size, then glides left and right
across the right-hand half at the top of the screen.  It uses slightly
different timing to make the movement of the two clouds more
interesting.

## The `RightRaindrop` sprite

This is more complicated than the "one thing at a time" version.  To
have more than one raindrop, we use _clones_.  The _original_ raindrop
is not visible.  Its job will be to launch clones of itself when the
right arrow key is pressed.  The _green flag_ script sets this up.

When the right arrow key is pressed, the raindrop needs to check a
couple of things before creating a clone:

* Only the original (hidden) raindrop should create a clone.  Without
  this check, every raindrop would create a new clone and we'd soon
  end up with far too many raindrops.  The code says to stop running
  the script (`return`) if this is not the original raindrop.

* We need to _not_ create a clone if there are already ten clones.
  The code says to stop running the script (`return`) if the length of
  the list of all clones is ten.

If those checks are OK, the code creates a raindrop clone.

When a clone is created, it runs the _when I start as a clone_ script,
which moves the (clone) raindrop to just below its cloud, shows
itself, then moves down the screen.  Once it's off the bottom of the
screen, we get rid of that clone.  As an experiment, delete the
`delete_this_clone()` line and make sure you understand what happens.
