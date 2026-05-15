# What is parallax?

Parallax is the effect where things closer to you move more quickly
across your vision.  Simulating this gives a strong 3D feel.


# Moving at different speeds

To make the parallax effect realistic, different layers need to move
at different speeds depending on how far away they should appear.

In this example, there are four moving "layers".  They all move at
different speeds:

 * The flowers move very quickly to make them appear close to the
   viewer.
 * The grass moves quite slowly, to make it appear quite far from the
   viewer.
 * The sky background moves very slowly, to make it appear very far
   from the viewer.
 * The clouds are a special case.  They move quite quickly, not
   because they're close to the viewer, but because they're being
   blown along by the wind.

The locomotive and its carriage stay completely still on the screen,
but the overall effect is that the train is moving through a
landscape.


# The code

To get the effect of infinite movement, we use two of each sprite, the
original and a clone.  Each one is wide enough to completely cover the
screen.  The code sets their positions so that they exactly join up.
Once one has moved completely off the screen, it moves back to the
right (completely off the screen) ready to smoothly move across the
screen again.  In this way, there are no gaps in what the viewer sees.

The various widths and speeds are all set up in one place, and then
all the sprites can have very similar code.


# Credits

Image Credits:

 * [CraftPix.net 2D Game Assets @
   OpenGameArt.org](https://opengameart.org/content/sunset-clouds-over-the-sea-pixel-background)
 * [Train artwork by Kooky](https://kooky.itch.io/pixel-train), used under
   [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
