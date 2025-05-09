class="y" Css Framework
=========================

Copyright (c) 2009, Colin Gourlay

class="y" is a simple fluid-width css framework for quickly injecting column-based grids into your html pages. Here's a quick example of class="y":

    <div class="y">
        <div class="x12 a">
            <p>Left Column</p>
        </div>
        <div class="x12">
            <p>Right Column</p>
        </div>
    </div>

In the code above, we have a div element with a class "y". This indicates that this element is a 'row' (it lies on the typical Y-axis of the document). The classes of the divs inside this element are prefixed with an "x" to indicate that they are 'columns' (they lie on the typical X-axis of the document). The numbers following this prefix can be translated to show how wide the column is, as follows:

* x12 = 1/2 of the width of the row
* x13 = 1/3 of the width of the row
* x14 = 1/4 of the width of the row
    
Columns are spaced by a margin equal to 1% of the row width. This margin is applied to the left of all columns, but it is not needed for the first column in the row. The first column in a row must also be assigned an "a" class so that this margin is not applied (there is a css pseudo-class that can be applied instead, but will not work across all browsers.

class="y" also provides a couple of extra column widths we can also use:

* x23 = 2/3 of the width of the row
* x34 = 3/4 of the width of the row

We don't have an "x24" class, as we can acheive the same effect by using "x12". These clases can be used in any order to acheive the effect we want. For example, if we want the first and last columns to take up a quarter of the row, and let the middle column span half of the row, we can mark it up as follows:

    <div class="y">
        <div class="x14 a">
            <p>Left Column</p>
        </div>
        <div class="x12">
            <p>Middle Column</p>
        </div>
        <div class="x14">
            <p>Right Column</p>
        </div>
    </div>
    
I'd experimented with more granular column layouts using 1/6th and 1/8th widths, but I decided to leave them out of this release of the initial release of class="y". They allowed even more complicated layouts, but they weren't consistently aligned across all browsers, and their implementation almost doubled the size of classy.css. If you desperately need them, you can request them by email, or take a few minutes to re-implement them yourself.

I hope you find class="y" useful.
