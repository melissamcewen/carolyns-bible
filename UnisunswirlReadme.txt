
If you want to see the Unisunswirl cat the way I intended, you will need to 
have the swirl.bmp in your game's Resource\catz directory.

This is a file which has been sound-stripped to make the download small.  

Because people with windows ME, XP etc have trouble with my small 
patches, I am now supplying all my breedz in this form, not just
my "species" (which have mostly been stripped, with external sounds).

What "sound stripped"  means is simply that there are no .wav files 
inside the breed.  Sometimes the game will play a "silent" sound from 
within it, and sometimes it will play a sound from within the game's 
originals, so your pets will sometimes look as if they are speaking 
(but make no sound) but not always.

Enjoy!

Carolyn Horn

P.S. If you want to put the sounds back in, and you are willing to use
a hex editor, you should be able to do so easily enough.  Just find the 
relevant base breed (you can usually tell which one I made a breed out 
of by comparing sizes in Windows Explorer).  Open that base breed and 
search for "Sounds root path" without the "" quotes (to find the 
sounds list).  Scroll to the bottom of that sounds list until you
get past the last WAV, and put the cursor in front of the first RIFF.  
Copy the whole of the section which starts with the first RIFF and 
finishes just above the naming area (hex 5004600). 

Find the same place after the sounds list in my sound-stripped file; 
you won't find the word RIFF, but put your cursor at the same
address and select the same number of bytes as you selected in the
base breed.  Now paste what you copied from that base breed, and save.

If all this sounds like double-dutch to you, then don't attempt it.  The 
breedfile works fine without sounds.
