
This file is intended for the use of hexers and anyone who wants to
change their Petz 3 Family Room.

Family Room.env is for use only in the English-language version of the game;
Wohnzimmer.env is for use only in the International versions of the game.

This Family Room.env file for Petz 3 will overwrite your game's original, and unless
you put everything in the correct place it _will_ crash your game, so please
please please make sure that you have your original safe somewhere and copies of
all your petz somewhere safe.

Place the Family Room.env in your game's resource\Area directory.  International-
language users place the Wohnzimmer.env in your game's resource\Area directory and
remove any other Family Room version you may have there for your own language.

Now unpack the included zipfile, called FamilyroomFilmstripsp3.zip, into your game's
main directory (the directory which contains the Petz 3.exe file)

The unzipping process _should_ create a set of subdirectories like the
ones shown in the included FamilyroomfilesWhere.jpg picture, with the needed files in

\art\Sprites\Area\FamilyRoom

If the unzipping process did not do that, then you will have to create the
directories manually, using Windows Explorer or My Computer, and place the files
in there.

What you should get are a load of .flm and .flh files -- these are the filmstrips
and filmstrip-info for the game.

Also in there are the Familyroom icon and the Familyroom backdrop.  These are simple
bitmaps and you can change these to whatever you wish in a paint program.
The Windows and fireplace filmstrips will still be in the same places; they will 
look the same.

Also included in the zip are a set of "prepared filmstrips". If you want to change the 
window or fireplace to something that looks different, take care to put the new items 
in the same place in the backdrop.bmp, and then edit the .bmp files of prepared filmstrips
in your favourite paint package.  When you've finished editing and saving these, open them 
into a hex editor and strip off the bitmap headers.  What needs to be removed is the first 
1078 bytes of each .bmp file.  You're not quite done yet, because the fireplace filmstrip
is made up from the switch followed by the fireplace itself, and each of the mouse lairs is
made up of two filmstrip sections.  So, open the header-stripped switch into your hex editor
and then open the header-stripped fire and copy/paste that onto the end of the switch. Save
as FAMILYROOM_FIRE.FLM.  Similarly add Laira2 to Laira1, save it as FAMILYROOM_LAIR_A.FLM,
and similarly with Lairb2 and Lairb1, save as FAMILYROOM_LAIR_B.FLM.  Now replace the
originals from my zip with your edited versions.

Have fun giving your petz nice new family rooms!

If you want to make it a separate playscene, you will need to give it a new ID number
and you will need to redirect internal information so as to prevent the fire in the 
original from clashing with the equivalent filmstrip in your edited playscene.

Cheers

Carolyn Horn


