# Playing the game

In this puzzle game, your goal is to end up with all the lights lit
except the centre one:

![The winning puzzle configuration](solved-game.png)

To do this, you can click on any of the lit-up lights.  When you do
so, that light goes out, but others around it flip.  "Flip" means that
if a light is off, it turns on; and if a light is on, it turns off.

Depending which kind of light you click, different other lights flip,
like this:

Centre light: a "plus" shape of lights all flip:

![Galaxy for centre star](centre-galaxy.png)

Corner light: a "box" shape of lights all flip:

![Galaxy for corner stars](corner-galaxies.png)

Edge-centre light: a "line" shape of lights all flip:

![Galaxy for edge-centre stars](edge-centre-galaxies.png)

The easiest way to see what this means is just to play a few times.

It is always possible to win, as long as the game doesn't by sheer bad
luck start off with all the lights off.  If that happens to you, just
click the green flag to start again.

This demo doesn't notice when you win.  That's up to you!

If you end up with all the lights off, then you're stuck and will have
to start again with the green flag.


# How the game works in Pytch

There are a couple of features of the code which might be of interest.

## Cells referred to by "index"

The two-dimensional layout is useful for humans, but doesn't really
matter once we know which cells affect which other cells when clicked.
(See the last section below.)  So the cells are just numbered across
then down from the top left, starting (as is typical in Python) with
zero.  Each clone has a variable `self.cell_idx` to store this
information.

## Remembering which star was clicked

Each clone of the `Cell` sprite might have to respond when any cell is
clicked.  To share the information about which cell was clicked, the
Sprite-level variable `Cell.clicked_idx` stores the index (see
previous point), but only while the click is being processed.  At
other times, this variable is the special Python "nothing" value
`None`.

## Putting the intelligence into data not code

To decide on the "galaxy" surrounding a clicked star, the code looks
up the required information in a list of lists, rather than a big
`if`/`elif`/`else` statement.  The code in the "when I receive
_flip-galaxy_" script is then very simple.

It can be a useful approach to store information in data not code.


# Where the game came from

The earliest reference to this puzzle game I could find is in the
[September, 1974 issue of _People's Computer Company_
magazine](./PCC-1974-09-pp14-15.pdf), where the game was called
_Teaser_.

The same puzzle was then presented as _Shooting Stars_ in the [May,
1976 issue of _Byte_ magazine](./Byte-1976-05-pp42-49.pdf), with an
implementation in 8008 assembler language.
