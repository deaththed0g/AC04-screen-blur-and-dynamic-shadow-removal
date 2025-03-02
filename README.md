# Ace Combat 04: Shattered Skies - Screen blur removal PNACH cheats

## About

Cheats for PCSX2-qt and 1.6.0 that will disable the screen blur effect that is applied to some cutscenes and missions.

The reason for removal is that PCSX2 doesn't yet correctly render the effect causing the issue known as "ghosting", which becomes more prominent as the user plays the game using higher internal resolutions.

![f01](https://github.com/user-attachments/assets/a0aa9271-f7eb-44ba-ad0f-a7e742c81327)

_The screenshot above was taken while the game was rendering at 12x its original internal resolution._

Besides removing the screen blur effect the PNACH files will also provide an option to remove the shadow that gets cast on the Player's aircraft if using PCSX2-qt while PCSX2 1.6.0 will remove both the screen blur effect and the shadow at the same time on activation.

At the moment of writing this section, latest nightly builds of PCSX2-qt [have greatly improved the emulation of the screen blur effect](https://www.moddb.com/games/ace-combat-04/news/ghosting-issue-almost-fixed-in-latest-pcsx2-qt-nightly-builds) although there are still some small visual artifacts visible when using the new graphic options.

**The PNACH files are only compatible with the US release of Ace Combat 04: Shattered Skies (SLUS-20152).**

## Usage

Go to your PCSX2's root directory then open the **CHEATS** folder. There, create a new _text file_ and name it **A32F7CD0.txt**.

***

### If using PCSX2-qt (aka 2.0):

Copy the following text lines inside the blockquote and paste them in the **A32F7CD0.txt** file we just created:

>[Disable screen blur]  
>author=death_the_d0g  
>description=Disable the screen blur effect used in some missions and cutscenes.  
>patch=1,EE,00111C4C,extended,24050000  
>patch=1,EE,001120BC,extended,DFBE0000  
>  
>[Disable aircraft dynamic shadow]  
>author=death_the_d0g  
>description=Disable Player's aircraft dynamic shadow.  
>patch=1,EE,00142500,extended,46000000  

Save the **A32F7CD0.txt** and rename it to **A32F7CD0.pnach**. 

Open the emulator, right click on Ace Combat 04's game icon, select **PROPERTIES** then **CHEATS**.

If everything was done correctly you should be seeing my cheats in the list.

![cg01](https://github.com/user-attachments/assets/ed49d3c1-b481-4b26-a391-2f85c7336c23)

Click on the small square next to the cheat entries under the **NAME** category to activate it. A tick means that the cheat is activated.

Close the window then run the game. The cheat(s) will take effect as soon the game is boot up.

***

### If using PCSX2 1.6.0:

Copy the following text lines inside the blockquote and paste them in the **A32F7CD0.txt** file we just created:

>[Disable screen blur]  
>author=death_the_d0g  
>description=Disable screen blur effect used in some missions and cutscenes.  
>patch=1,EE,00111C4C,extended,24050000  
>patch=1,EE,001120BC,extended,DFBE0000  
>patch=1,EE,0020E660,extended,24070000  
>  
>[Disable aircraft dynamic shadow]  
>author=death_the_d0g  
>description=Disable Player's aircraft dynamic shadow.  
>patch=1,EE,00142500,extended,46000000  

Save the **A32F7CD0.txt** and rename it to **A32F7CD0.pnach**.

Open the emulator, go to the menu bar and click ON **SYSTEM** then click on **ENABLE CHEATS**.

Run the game. The cheat(s) will take effect as soon the game is boot up.

***

If you have a PNACH file for AC04 already, just copy the lines inside the blockquote and paste them at the end of the it then save the file.

## Notes

- Disabling the dynamic shadow in PCSX2-qt is _completely optional_. While t might not properly render at higher internal resolutions at least will not cover the entire aircraft like it does when emulating the game using 1.6.0.

- Using the 1.6.0 version of the PNACH files will also remove the blur effect in the **STONEHENGE OFFENSIVE** mission, caused every time the S.T.N turrets fire their railgun.

- The PNACH file for 1.6.0 will also completely remove the dynamic shadows that causes the **"black plane"** issue.

- To fully restore the disabled effects, a game restart will be required after disabling the cheats. For PCSX2 1.6.0, you'll need to remove the lines you copied from this article from the PNACH file.

## Special thanks

- **BelkanLoyalist** ([Twitter](https://twitter.com/BelkanLoyalist)/[ModDB](https://www.moddb.com/members/justauser1)) for testing the cheats.

## Further reading

[Justin EL's](https://www.youtube.com/@justinels9591) [Ace Combat Emulation Guide](https://docs.google.com/document/u/0/d/1PKzXTElL_UoSS-nZk7G0eyNhSOOSNDuiqdSb1aMNx0Q/mobilebasic?pli=1#h.qdjr9pqjitis) to configure PCSX2-qt and get the best emulation possible for the Ace Combat games.
