# Images for galaxy shapes

The Inkscape file was manually adjusted then the selection exported to
get the `star-*.png` files.  From there, scale them all to 180 wide
with some transparent padding:

``` shell
parallel \
  convert {} -resize 150x150 -gravity center -background none -extent 180x180 w180-{} \
  ::: star*
```

Then the centre one re-done to be 360 wide:

``` shell
convert \
  star-4.png -resize 150x150 -gravity center -background none -extent 360x180 \
  centre-galaxy.png
```

Then the others assembled into the other two galaxy shapes:

``` shell
convert \
  '(' w180-star-0.png w180-star-2.png +append ')' \
  '(' w180-star-6.png w180-star-8.png +append ')' \
  -append \
  corner-galaxies.png

convert \
  '(' w180-star-1.png w180-star-7.png +append ')' \
  '(' w180-star-3.png w180-star-5.png +append ')' \
  -append \
  edge-centre-galaxies.png
```

Then remove the `w180-*.png` files.
