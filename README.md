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


## Development notes
- [Initial printer calibration](calibration.md)
- [Graph paper base with crosshairs](graphbase-crosshairs.ps)
- [Machine-readable section markers](sections.md)
