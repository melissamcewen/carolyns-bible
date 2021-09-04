
This part of my "easy-edit" range.  I've made this easy-edit
toy so as to help people who have trouble understanding my
advanced filmstrip-editing tutorial.

These treats will show up separately from the Candy Hearts,
so they won't overwrite.  They look just the same (well, almost--
I made a small change to the box in order to check that the system
worked).

If you unpacked this zipfile into your game's main directory (where
the .exe is), it should create a nest of directories, off that main
directory, which goes like this:

\art\sprites\Toyz\Tbox_i1

And there should be several .flm, .bmp, and .txt files in that final
Tbox_i1 directory.  If you unpacked this elsewhere -- such as the 
game's \resource\Toyz directory -- it should have created that nest of
directories off of that one, and you will need to move it.  In
Windows Explorer or My Computer you can move the art directory (and
it's subdirectories will go with it) by right-clicking on it, dragging,
and dropping it where you want it to go (in this case the game's main
directory).

Place the .toy file in your game's \resource\Toyz directory of course.

Run the game and check that the treats are actually there.  If so,
all is well and you can start to edit the filmstrips.

The 11 .bmp files are the filmstrips prepared with bitmap headers, and
you can edit them in your favourite paint package.  Whenever you save,
choose "save" not "save as".  When you've finished, move the .flm files 
away from that directory (or rename them).  Now rename

Trea_i1flm.bmp Trea_i2flm.bmp Trea_i3flm.bmp to
Trea_i1.flm Trea_i2.flm Trea_i3.flm

And now you have to do something simple in a hex editor.  Open Trea_i1.flm 
into the hex editor and delete from the top of it the first 1078 bytes.
Save it.  Do the same for Trea_i2.flm and Trea_i3.flm.

Open Away1.bmp into the hex editor and delete from the top of it the first
1078 bytes.  Save it as TBOX_i1_AWAY.FLM.  Place your cursor at the
end of it.  Now open Away2.bmp into the hex editor, go to the point directly 
after the 1078'th byte and select from there to the end. Choose
Copy.  Go back to the new TBOX_i1_AWAY.FLM and Paste at the end of it.
Save.

Go through the same process with the six treats .bmp files, starting by
stripping those first 1078 bytes from the top of treats1.bmp and saving
it as Tbox_i1.flm.

Now run the game and take out your nifty new toy, which even shows up
separately on the shelf!

You can edit the .txt files also, of course, in any text editor.

Enjoy!

Carolyn Horn