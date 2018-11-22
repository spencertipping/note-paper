# Section markers
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
unambiguous. Let's go with dimensions that align with the graph cells.
