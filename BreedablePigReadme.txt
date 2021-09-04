
To get Pigz to breed
--------------------

When your pigz are obviously very fond of each other and ready to breed, close the game.  Put the Pig.dog file that you were using somewhere safe -- either one of the "fixed" versions or the game's original -- you'll want it again.  Now put in its place the one from my BreedablePig_d5.zip file.  Open the game and watch your pets announce their happy event.  They will be largely silent during this period, but they will breed.  You can use the appropriate normal Pig.dog breedfile to watch your pigz play, but you will need the breedable file in place again when it's time for the babies to be born, and again when they are ready to separate from their mother.

Remember that when playing with this breedfile in place, you will need to either turn off the "Hosts in Playscenes" option or avoid the Backyard and Fantasy Castle, as the game's Host pig will crash the game.

Enjoy!

Carolyn Horn

NOTE -- for people who don't want to download one of my PigFixes but do want to adopt or import pets, here's a copy of the "Howto":

Making pigz adoptable and still being able to play with the Host
----------------------------------------------------------------

You can adopt Pigz from the Adoption Centre in Petz 5 if you alter one byte in the breedfile:

0000F4E0 0000 0000 5769 6C62 7572 0000 0000 0000 ....Wilbur......
0000F4F0 0000 0000 0000 0000 0000 0000 0000 0000 ................
0000F500 0000 0000 FC03 0000 1900 0000 0000 0000 ................
0000F510 424D C429 0000 0000 0000 3604 0000 2800 BM.)......6...(.

in place of 

FC03 0000 1900 

put 

FC03 0000 0100

The pig will then come out without problems, and will not be neutered when you adopt it.

I believe that they will not breed using this particular breedfix; I certainly have never found them to do so, and I think that the necessary brhaviour is missing.   But you can definitely adopt pets with it and you  will find that the Host in the backyard/ Fantasy Castle will still appear without problems.  You should be able to use my "Breedable Pig" file to breed these pigz.

IMPORTANT
---------
Don't try this with the bunnies!  You can change the byte and adopt them -- but when the game has closed the petfile will crash the game if you try to open it with the bunny pet in place.  I believe that this is because the bunny uses the same icon as the pig.  I do not yet know if this is fixable within the official bunny file.

Making it so that adopted Pigz from previous games can be imported
------------------------------------------------------------------

NOTE: With this fix, I'm sorry to have to say that you cannot play with the Host Pig.  The game will crash if that Host tries to come out.  So if you are importing pigz or Pigz mixes, turn off the Hosts in Playscenes option or avoid the Backyard and Fantasy Castle.

Where I show you in the above example 

FC03 0000 1900 

Put instead 

FFFF 0000 0100

Pigz using this breedfile fix will also probably not be able to breed.  However, as with the fix above, you can use my "Breedable Pig" fix to breed the imported pigz and pigz mixes.





