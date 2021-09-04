
This zipfile contains split filmstrips for your game's carrycase and its door, 
also the Adoption Centre and its doors.

It is intended that you use this along with my easy-edit package, so that you
won't have to re-insert the files into the game's .dll but can just put the finished,
edited filmstrips into the relevant directory on your hard drive (see the easy-edit
package to see where they should go).

To edit the filmstrips you'll need to understand something about filmstrip
editing.  I have tutorials about that; you would want the advanced filmstrip editing
tutorial. For the Case filmstrips, I've also provided them with bitmap headers so 
that all you need to do is edit them, strip off the headers and put them together again 
as Case.flm to overwrite the one in your game's \art\sprites\case directory.

The idea for each of these sets of filmstrip sections is that you attach the blank bitmap
header to the top of each filmstrip section in a hex editor, then edit the bitmap header
using the info .gif or .jpg files to give you the total bytes and the number of rows for
each filmstrip header.  If you haven't a clue what I'm talking about, please do read
my filmstrip-editing tutorial, with any luck that will help.  Once you have the bitmap header
in place and correctly edited, you can then open the filmstrip section in a paint package
of your choice and edit it to make your own creation.  Then you will need to strip
off the bitmap headers again and stick all the filmstrip sections together in the hex
editor, starting with number 1 (i.e. adptflm1) and continuing until the last one in that
series (i.e. adptflm4).  NOTE -- the casedoor has 13 sections, ending with casedoor14(key).
Yes, I know there isn't a casedoor05; that was a mistake in numbering on my part.  either
I can't count or I had a brain-fart...  Sorry about that.  There are only 13 sections, honest.

Enjoy!

Carolyn Horn