# Sierpinski Pyramid in PostScript

This is a PostScript program that draws the famous fractal object with a
specified orientation and shading.

PostScript is not a great general purpose language by today's
standards. Things are unnecessarily difficult. Built-in functionality is
missing for things that should be trivial: named parameters, local
variables, infix expressions, string/array concatenation, growable
arrays, functional features like map and filter, etc. These can all be
implemented, but the code turns out ugly and is painstaking to write,
with widely varying styles and idioms.

But the graphics are neat and that's what it's for. Most PostScript code
is automatically generated and obfuscated anyway.

I wrote the first simple version of this at Carnegie Mellon in 1995
(`pyramid-cmu1.ps`) including simple perspective
(`pyramid-cmu1p.ps`). These versions were quick and simple and worked by
drawing in two shades from back to front.

In 2020, I resurrected it and changed the orientation of the outer
pyramid (`pyramid-cmu2.ps`). Instead of calculating the vertex
coordinates as complicated rooty values, the coordinates match 3D
integer gridpoints:

> (+1, +1, +1)
> (+1, -1, -1)
> (-1, -1, +1)
> (-1, +1, -1)

Then I went overboard and added 3D rotation, sorting and rendering of
individual faces, and a lighting model. I did stop short of movable
viewpoint, shadows, raytracing, etc.

## Running

The raw PostScript file can be sent to a printer, or it can be displayed
using Ghostscript: `gs pyramid.ps`

# Output

![](clip.png)

## Meta

Curt McDowell - <coder*fishlet,com>

Distributed under the Apache 2.0 license.
See ``LICENSE-2.0.txt`` for more information.

[https://github.com/curtmcd/pyramid](https://github.com/curtmcd/)
