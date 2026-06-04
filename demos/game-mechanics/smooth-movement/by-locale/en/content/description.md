# Simple movement without limits

You can move the pig with the `wasd` keys.  It moves smoothly, but a
problem is that you can move it completely off the screen.

## Explanation of the code

The pig's script sets the starting position of the pig.  Then it loops
forever, checking whether the `w`, `a`, `s`, or `d` keys are pressed,
and moving slightly (by changing the _x_ or _y_ coordinate) if they
are.  The amount of movement is set by the `speed` variable.  It's
useful to keep that number in a variable even though it doesn't
change, because it makes the code easier to adjust and to read.


# Simple movement, staying on the screen.

You can move the cow with the arrow keys.  You can't move it outside
the screen.

## Explanation of the code

The code is very similar to the pig's.  The new parts are:

* We have a variable `x_limit` to say how far left and right the cow
  can move.  In the loop, we only allow rightwards movement if the
  cow's _x_ coordinate is less than `x_limit`.  We only allow
  leftwards movement if the cow's _x_ coordinate is more than
  `-x_limit` (the negative of `x_limit`).

* We have a variable `y_limit` which does a similar job for up and
  down movement.


# Movement with inertia

You can move the goat with the `ijkl` keys.  It takes a small amount
of time to speed up or slow down.

## Explanation of the code

The goat's code is the most complicated.  We keep track of the goat's
_velocity_ in the left/right and up/down directions.  Velocity is very
similar to speed, but velocity includes which direction the goat is
moving.

Pressing `i` does not directly move the goat up.  Instead, it
increases the `y_velocity` by the value of the `accel` variable, up to
a limit.  Similarly, pressing `k` decreases the `y_velocity`.  If
neither `i` nor `k` is pressed, the velocity changes towards zero.

We do the same thing for left/right movement, adjusting the
`x_velocity` variable.  Then we change the _x_ coordinate by the
`x_velocity` and the _y_ coordinate by the `y_velocity`, but make sure
the goat does not go outside its limits.

We use Python's `min()` and `max()` functions to make sure the two
velocity variables don't get too big, and to make sure the goat
doesn't move off the screen.


# Credits

Thanks to Pexels user [Damir K.](https://www.pexels.com/@damir/) for
the field photo (which we have cropped and adjusted), and to
[FreePixel.art](https://freepixel.art/) for the animal graphics.
