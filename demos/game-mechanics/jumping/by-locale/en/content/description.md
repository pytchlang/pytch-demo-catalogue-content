# Left and right movement

How the sprite moves is not the main point of this demo, but it might
be useful to look at the way we change the costume to make the
character face the direction it's moving.  The code does not check for
where the character is on the screen, so you can move it off the
screen.


# Jumping

The character jumps when you press the "space" key, so the code is in
the _when space key pressed_ script.  The main logic for jumping is
the section involving the `y_velocity` variable.  We move the
character up quite quickly at the start, changing its _y_ coordinate
by 8.  Then we reduce the velocity down to zero, and through zero to
-8, to move the character back down to earth.  All these changes to
_y_ add up to zero, leaving the character at exactly the same height
it started.  This whole process mimics the way gravity works.


# Avoiding double-jumps

We want to make sure the character doesn't start a new jump while it's
in the middle of a previous one.  The code uses a Boolean `jumping`
variable to track this.  Initially (_when green flag clicked_), the
character is _not_ jumping, so `jumping` is `False`.  In the _when
space key pressed_ script, we first check whether the character is in
the middle of a jump, and stop running that script if so.  Then we set
`jumping` to `True` while the up and down movement is happening, and
back to `False` once that's done.


# Credits

Thanks [GrafxKid](https://opengameart.org/content/green-robot) for costume!
