# Collecting boxes

The forklift can collect a box by touching it before it leaves the screen.
Once the player does so, the forklift's friction on the ground changes slightly, making turns more difficult.

# Delivering

Once the player has collected three boxes, they need to drop off their boxes at the delivery truck near the 
right side of the screen. Only after dropping off the boxes will the `self.score` variable in the `scorekeeper` sprite
increase.

# Movement and friction

The forklift in this demo can move left and right but also slows down over time if no button is pressed or the forklift changes its direction.
This means that if the player lets go of the A and D keys they pressed before, the forklift will still move a little bit
into the previous direction before eventually stopping or moving into the other direction.
This is done by multiplying the `self.speed` variable in the `when I receive "game-start"` script of the `forklift` sprite
with a number between 0 and 1. The closer the number is to 1, the lower the friction is and the longer the forklift takes to slow down.
This makes the movement feel slippery, adding to the challenge of collecting boxes. The code checks for the position of the forklift so that it cannot move
outside the screen.

# Credits

Thanks to Lauryn from Tallaght Community School for working on this demo
and allowing us to make edits and publish it.