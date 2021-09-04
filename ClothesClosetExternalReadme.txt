
This file is intended for the use of hexers and anyone who wants to
change their Petz 3 Clothes Closet.

Clothes Closet.env is for use only in the English-language version of the game;
Kleiderschrank.env is for use only in the International versions of the game.

This Clothes Closet.env file for Petz 3 will overwrite your game's original, and unless
you put everything in the correct place it _will_ crash your game, so please
please please make sure that you have your original safe somewhere and copies of
all your petz somewhere safe.

Place the Clothes Closet.env in your game's resource\Area directory.  International-
language users place the Kleiderschrank.env in your game's resource\Area directory and
remove any other Family Room version you may have there for your own language.

Now unpack the included zipfile, called petz3ClothesClosetFiles.zip, into your game's
main directory (the directory which contains the Petz 3.exe file)

The unzipping process _should_ create a set of subdirectories with the needed files in

\art\Sprites\Area\ClothesCloset

If the unzipping process did not do that, then you will have to create the
directories manually, using Windows Explorer or My Computer, and place the files
in there.

What you should get are a .flm and a .flh file -- these are the filmstrip
and filmstrip-info for the game.

Also in there are the  icon and the backdrop bitmaps.  These are simple
bitmaps and you can change these to whatever you wish in a paint program.
The closet filmstrips will still be in the same places; they will 
look the same.

Also included in the zip are a set of "prepared filmstrips". They are in the zip called 
petz3ClothesClosetfilmstrips.zip.  If you want to change the closet  to something that looks 
different, take care to put the new closet and buttons in the same place in the backdrop .bmp 
file, and then edit the .bmp files of prepared filmstrips in your favourite paint package.  
When you've finished editing and saving these, open them into a hex editor and strip off the 
bitmap headers.  What needs to be removed is the first 1078 bytes of each .bmp file.  

You're not quite done yet, because the full CCLO filmstrip is made up from three filmstrip sections.  
So, open the edited and header-stripped cclo1flm into your hex editor and then open the edited 
and header-stripped cclo1flm and copy/paste that onto the end  of the first. Then open the edited 
and header-stripped cclo3flm into the hex editor and copy/paste that onto the end of the combined 
cclo1flm/cclo2flm one.  Save as CCLO.FLM.  Now replace the original from my zip with your edited version.

Have fun giving your petz nice new clothes closets!

I would advise you not to try making it a separate playscene with its own ID number, as 
the game might crash if it contains two functioning clothes closets.  Nothing to stop you
from putting different filmstrips into it, disabling the clothing, and then having it as a
separate one of course; experiment as much as you wish, the worst that can happen is a few
game-crashes while you try things out :-)

Cheers

Carolyn Horn


