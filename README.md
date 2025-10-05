# CoCo2

This is my version of two separate composite video mod boards for the Tandy Color Computer 2, based initially on calphool's work.  One board is, like his, to replace a vertical RF Modulator, the other is to replace a horizontal RF Modulator.  The circuit design is the same for both.

I started with calphool's work, but re-did the whole board in KiCad.  The vertical board has some support PCBs that can be fabricated, and they serve as grounding points... You can use the board without them, but you'd need to use a grounding wire.  Horizontal board is mounted by taking a solder lug, bending the tab 90 degrees, and screwing it up into the board through the standoff (which should be soldered from the top for the best strength).
![Lug Mount](solder_lug_mount.jpg?raw=true)
Grounding seems to work great so far, we'll see if I have issues with it backing out.  This is the first time I've tried doing anything with KiCad, so... hopefully it's not terrible.

With some advice from captainkirchoff in Discord, I've tweaked some resistors and added a circuit that let the channel select switch disable color.  Please note that this is really only for monochrome monitors, as it completely suppresses the chroma signal, which causes some weird artifacting in many color monitors.

Vertical version has also had a switch added to replicate the same functionality for that board... I used a SLW-1298856-5A-RA-N-D (will be in the BOM) - Had to import the footprint for it, so if you work on the board you'll need to grab that library from them.

Note that you can increase the value of the C4 capacitor and get better noise reduction (suggested value can go up to 10uF), but ceramic caps are still preferred.

The vertical board's support brackets are set up so that you can slip a thin metal tab (I cut a piece off of one of the solder lugs in the BOM) into the slot after it's slotted into the board, then you add solder to create the joint.
![Vertical Board Support Joint](vertical_board_support_joint.jpg?raw=true)

Overall fitment suggestion would be to solder the smaller supports to the back side of the board along with the headers (the size of header is VERY important, the BOM has the right size) - Then you slip it into place on the board with the longer supports just dry fit.. make sure everything is where you want it, then solder the longer supports into place, and finish by soldering the underside of the motherboard.  On mine, this resulted in a very solidly mounted board that would hardly wiggle.

https://www.digikey.com/en/mylists/list/GH709EISJW - This is the parts list for the board, with the updated transistors to make sure they were options that would be available and an audio jack that should fit the footprint I had on the board.

# Horizontal Board pics

![Horizontal Board Top](horizontal_board_top.jpg?raw=true)
![Horizontal Board Side](horizontal_board_side.jpg?raw=true)

#Vertical Board pics

![Vertical Board Top](vertical_board_front.jpg?raw=true)
![Vertical Board Side](vertical_board_back.jpg?raw=true)
