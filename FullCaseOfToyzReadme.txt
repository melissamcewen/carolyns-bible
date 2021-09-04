
If you want to play the game as intended and use the mini-games to gather stuff, then don't bother with this!

This is to help people who want to play Petz 5 without having to search for all the toyz or play the mini-games, or who have already done so but had to re-set their game and can't face starting all over again.  It will also help people who want to add their own custom-made toyz etc.  

Okay, what you should find in this zipfile are:

Case NameInfo.lkv
caseForWin95-98.reg
caseForXP.reg

1) Place the Case NameInfo.lkv file in your game's Resource\keys directory.

2) Choose the _correct_ .reg file for your Operating System and double-click on it.  This will automatically place the hexadecimal number 77 in the "Case ListSize" string.  IMPORTANT: Choose the .reg file which is right for your operating system; do not touch the other one!  I believe that the Windows ME OS uses the same format of .reg file as Win 95/98, but it would be best to check before trying it.  Similarly with Windows 2000.  If you want to use one of these .reg files with ME or 2000, then you could find out which one is right for you by exporting a small registry key (Open Regedit.exe and navigate to any key by clicking on the little crosses, and choose "Export" from the Registry menu).  Find the exported file on your hard drive, rename it to xxx.txt, and open it in Notepad.  If it has REGEDIT4 at the top, then you can use the "caseForWin95-98.reg" file.  If it has W i n d o w s   R e g i s t r y   E d i t o r   V e r s i o n   5 at the top, then you need the "caseForXP.reg" file.

OR you may prefer to enter the number manually:

If you would rather enter the number manually, then open Regedit.exe and navigate via the little crosses at the sides of the names to here:
HKEY_LOCAL_MACHINE\SOFTWARE\StudioMythos\Petz 5\4.00.00
Click on the 4.00.00 so that you see a load of stuff in the right-hand pane; scroll down that side until you see Case ListSize.  Double-click on that name and a tiny hex editor will open with four numbers, three of which are 00.  Higlight the first of the numbers (which will probably be 07 or higher) by putting your cursor on the left of it and dragging to the right of it.  Enter the number 77.  Close Regedit.

A warning here; you are very unlikely to mess up the registry just dabbling around in this particular area, but it is _always_ advisable to make sure you have a backup copy or a recent Rollback just in case.

3) Run the game; you will now see all the toyz that would nromally have been in the toy closet (if Petz 5 had had one), or at least most of 'em.  

4) If you've done all that and the case doesn't show up full, then you need to re-set the registry settings for the game.  You do this by holding down the Shift and Ctrl keys on your keyboard whilst starting the game.  After the registry has been re-set in this manner, go through the steps for making a full toy case again; double-click on the .reg file and place the "Case NameInfo.lkv" in the resource\keys directory.


How to add your own:
==================
If you make or download a new, hexed toy, you will want to see it right away in the case.  First of all, it does have to have its own name and an ID number which doesn't clash with the others of course.  But then you have to add it to the Case NameInfo.lkv file.  To do this, just open it into a hex editor and select the last item in the list.  By this I mean, go to the end of the list where you see the last instance of \Resource\Toyz, put your cursor directly before that, and select from there to the end of the file.  It will be 260 bytes.  Choose Copy.  Now place your cursor at the end of the file and choose "Paste".  Save.  Now change this duplicate toy's name to that of the one you want to see in the game.  Finally, either edit the little .reg file mentioned above or directly edit the registry so that the number 77 is now 78 (remember we're talking hex numbers, by the way, so if you gradually add even more toyz, the number will increase from 78 to 79, then 7A, etc).  Now if you run the game, so long as the toy is not a "hidden" one or corrupt in some way, it will appear in the case.

Note on Petz 5 toyz generally:
===========================
I may have missed one or two in my list, so of course you can change it as above if you find one missing.  Or I might have listed one or more that is in fact a hidden toy, which of course won't show up unless you change the "hidden toy" byte.  This "hidden toy" byte works the same as it does in Petz 3 and 4, by the way, as indeed does the basic structure of the toyz.  You still have the header stuff followed by the listing of what's in the file, with the sprite names and ID number ("offset byte") directly below that.  As before, for making a toy be "unhidden", you change the hex "01" which is three bytes after the ID to "03"

After the ID area, we get (as before) the graphics of the toy.  In a few cases, such as the dear old auto-rolling ball, the graphics are in the familiar form of .lnz files, i.e. they are all ballz and linez just as with clothes and breedz; these will be easy to edit into attractive new toys.

In most cases, however, the graphics are in the form of a filmstrip.  This is where things have changed a little, due of course to the fact that the graphics are now 24-bit instead of 256-colour.  Instead of being in the form of "FLH" information followed by "FLM" graphics, they are now in the form of "SPR" files, each of which contains data which is very like the old "FLH information, plus the graphics themselves.  This makes them a bit muddling, as it's not easy to find the beginning and end of each actual graphic section.  So the good news is that they do appear still to be in the form of a series of bitmap frames which _can_ be stripped out and given a 24-bit bitmap header; the bad news is that they are not as  simple to strip out and give headers as the 256-colour ones were.  And although it _is_ possible to recolour them by changing bytes, the colour results are unpredictable -- there isn't a palette in quite the same way as for the 256-colour bitmaps.

And finally, of course, the renaming section of the file is the same; just do a search for the hex string 50004600 and that will get you down to the part which looks like this:

00113632 0000 1700 2800 6300 2900 2000 3100 3900 ....(.c.). .1.9.
00113648 3900 3700 2000 5000 4600 2E00 4D00 6100 9.7. .P.F...M.a.
00113664 6700 6900 6300 2C00 2000 4900 6E00 6300 g.i.c.,. .I.n.c.

and, as with the earlier petz games, the name to change when making a new toy is directly below that.

Happy playing, and happy hexing

Carolyn Horn
