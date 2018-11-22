# Note paper
I could buy graph paper, but it's cheaper to print your own -- particularly
because it uses almost no ink/toner. While I'm at it, I'd also like to customize
the layout a little bit.

First, I take notes in a sort of unusual layout. I'm left-handed so I'll take a
half-sheet (usually a full sheet folded in half) and make three sections, each
facing a different direction:

    +---------------------------------------+
    |         ^           |                 |
    |         |           |   section 1     |
    |     section 3       |      |          |
    |---------------------|      |          |
    |                     |      V          |
    |          section 2  |                 |
    |           <------   |                 |
    |                     |                 |
    +---------------------------------------+

This creates some problems for scanning because there's no metadata about which
notes face in which direction. So ideally I can solve this problem by adding a
few things:

1. Markers for the section boundaries
2. Directional markers per section
3. Sequence indicators so notes are chronologically ordered


## Section markers
We need something that (1) the computer can read, and (2) I wouldn't draw by
hand into my notes. It should be self-aligning and tolerate some rotation and
scaling due to printer and/or scanner imperfections -- and it needs to indicate
the size of the section as well as the direction of text within it.

I think the simplest strategy is to use a block of three dots, where the third
one has some difference:

    ####  ####  #
    ####  ####  ##
    ####  ####  ###

This can be followed by smaller dots that encode the sequence number of that
section within the stack. For instance, maybe this would encode section number
185 (`ffeedd...11` wouldn't appear on the page):

                         ffeeddccbbaa998877665544332211
    ####  ####  #                        ##  ######  ##
    ####  ####  ##
    ####  ####  ###

We probably also want some printed margins around sections to make it clear what
will be scanned and what won't.

A medium-point pen is 1mm, so anything significantly larger than that should be
unambiguous. Let's go with 4mm for the sides of the three-dot indicator, and 1mm
for each of the bitwise dots after that.


## Graph lines
I prefer a small graph ruling, about 0.2" per cell. Sometimes the lines are
heavier than ideal, so I'm considering doing something like shading the
crosshairs more heavily than the cell boundaries:

```
        |           |
- - - --+-- - - - --+-- - - -
        |           |
        .           .
        .           .
        .           .
        |           |
- - - --+-- - - - --+-- - - -
        |           |
        .           .
        .           .
        .           .
```

That way the alignment cues are still there, but there's less visual clutter on
the page.
