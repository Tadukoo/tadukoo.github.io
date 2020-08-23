---
title: T.A.D.U.K.O.O. I.S. T.H.E. G.R.E.A.T.E.S.T. P.E.R.S.O.N. W.H.O. E.V.E.R. L.I.V.E.D. Old System Changelog
project: TAG
index: 1
---
There was a different versioning system for the first batch of revisions.

#### Table of Contents
* [v.0.0.0](#v000)
	* [R1](#r1)
	* [R2](#r2)
* [v.0.0.1](#v001)
	* [R3](#r3)
	* [R4](#r4)
	* [R5](#r5)
	* [R6](#r6)
	* [R7](#r7)
	* [R8](#r8)
	* [R9](#r9)
	* [R10](#r10)
	* [R11](#r11)
	* [R12](#r12)
	* [R13](#r13)
	* [R14](#r14)
	* [R15](#r15)
	* [R16](#r16)
* [v.0.0.2](#v002)
	* [R17](#r17)
	* [R18](#r18)
	* [R19 Special Edition](#r19-special-edition)
* [v.0.0.3](#v003)
	* [R20](#r20)
	* [R21](#r21)
	* [R22](#r22)
	* [R23](#r23)
	* [R24](#r24)
	* [R25](#r25)
	* [R26](#r26)
	* [R27](#r27)
	* [R28](#r28)
	* [R29](#r29)
	* [R30](#r30)
	* [R31](#r31)
	* [R32](#r32)
	* [R33](#r33)
	* [R34](#r34)
	* [R35](#r35)
	* [R36](#r36)

Started working on November 26, 2014 9:44 AM

## v.0.0.0

### R1
* Released: November 26, 2014 11:18 PM
* Setup Framework for the game.
* Implemented up and down collision checking and Player position correcting.
* Basically I edited the Moonlander game code I had to not be moonlander and have stuff I needed for my game.
* Possibly introduced Issue # 6: Being in the perfect spot on the edge of a platform causes the Player to clip through it.
* Introduced issue that moving on a platform has you vibrating up and down.

### R2
* Released: November 27, 2014 10:47 AM
* Implemented left and right collision checking and Player position correcting.
* Testing on May 27, 2016 at 11:13 AM revealed that Issue # 6 is present in this version (it's believed to have started in R1, but hasn't been demonstrated in 
that version yet).

## v.0.0.1

### R3
* Released: December 7, 2014 8:56 PM
* More collision checking and Player position correcting.
* This was for improving the collision detecting and position correction.
* Now your character vibrates up and down by 1 pixel when standing still on a platform.
* Now you get pushed far enough to the left/right that you aren't on the platform.
* First version to have a version number (v.0.0.1R3).

### R4
* Released: December 8, 2014 12:58 PM
* Solved issue of player vibrating on platforms.
* Added corner collision detection and position correction to try to make smoother corrections.
* Discovered Possible Issue # 1.

### R5
* Released: December 8, 2014 8:31 PM
* Made a solution for Possible Issue # 1.
* You now lose speed when colliding with a wall when jumping up.
* Made changes that sped up the game, but sprite sizes were going to change soon, so it wasn't decided yet if this was good or bad.
* Made title sequence of scrolling through the long title, currently at least 10x faster than the final will be.
* Planned to make the final title sequence have game elements in it.

### R6
* Released: December 10, 2014 10:19 AM
* Game is now fullscreen.
* Can hit escape to exit the game now.
* Decided the movement is too fast.
* Can no longer make it to the middle platform from the lower one (at least on my resolution, scaling isn't implemented yet).

### R7
* Released: December 10, 2014 11:19 AM
* Speed now has a cap.
* You can move faster by holding down shift.
* You can no longer go off screen to the left (you can still to the top, bottom, and right).

### R8
* Released: December 10, 2014 10:26 PM
* Changed background to a sky with clouds.
* Changed player to facing right sprite of Tadukoo.
* Changed platforms sprite to be a yellow box with lines going vertical, horizontal, and diagonal through them.

### R9
* Released: December 11, 2014 9:37 AM
* Slowed movement (to scale it down like the sprite sizes).
* Extended bottom platform to be across the whole bottom.

### R10
* Released: December 11, 2014 10:28 AM
* Established scaling system.

### R11
* Released: December 11, 2014 11:54 AM
* Added dying when you fall past the bottom line.
* Causes you to die from jumping because of faulty collision correction.
* Issue # 3 pointed out as a problem: Player appearing to clip through blocks before being corrected.
* Previously wasn't needed as much. Introduced in Pre-Alpha v.0.0.0R1.

### R12
* Released: December 11, 2014 12:59 PM
* Fixed Issue # 3.
* Also fixed speed being increased with more platforms being added into the game.
* Collision checking was when the Player's position was updated, making it weird.

### R13
* Released: December 11, 2014 3:30 PM
* Added gap in bottom platform so you can fall off (for testing that works)
* Added Lava that damages you (looks like fire though).

### R14
* Released: December 11, 2014 9:21 PM
* Tried making slowing effect for Lava, but failed.
* This is Issue # 4.

### R15
* Released: December 11, 2014 9:28 PM
* Fixed Issue # 4, but introduced Issue # 5.
* Issue # 5: Player bounces up and down in Lava, as if it's water, and dies.

### R16
* Released: December 11, 2014 9:41 PM
* Fixed Issue # 5. Now Lava works as intended.

## v.0.0.2

### R17
* Released: December 11, 2014 9:47 PM
* Changed Platform sprite.
* Added Player death sprite.
* Discovered Issue # 6: Player's edge being on the edge of a platform allows you to clip through it.
* This was there since R1, but wasn't found before.

### R18
* Released: December 11, 2014 10:15 PM
* Fixed Issue # 6.

### R19 Special Edition
* Released: December 12, 2014 11:54 AM
* Added background of my selfie on main menu.
* Changed Platform sprite.

## v.0.0.3

### R20
* Released: December 12, 2014 2:13 PM
* Removed selfie background
* Added buttons on main menu
* Removed hitting escape to exit on main menu
* Buttons light up when selected (blue for good, red for bad)
* Cursor to show what button is selected (an arrow)
* Buttons include Play, Tutorial, Options, and Exit.
* Tutorial and Options are unavailable.

### R21
* Released: December 12, 2014 5:47 PM
* Added debug key combination (control, shift, T, V)
* Made it so player debug information only shows if debug is true.

### R22
* Released: December 12, 2014 7:22 PM
* Added knee spasm graphics
* Player is sad and knees go between 3 frames.
* Currently default for testing purposes.

### R23
* Released: December 12, 2014 11:41 PM
* Moved test level to be hidden (currently no way to get to it without modifying code)
* Created bedroom level.

### R24
* Released: December 13, 2014 11:38 AM
* Added bed, which you can interact with using E.
* Short dialog of Tadukoo and his mom when using bed.

### R25
* Released: December 13, 2014 12:52 PM
* Created Home class for use with chapter 1
* Now Game uses Home class rather than Bedroom
* You can now get to the test area through the main menu through an easter egg of pressing the correct arrow/wasd keys.

### R26
* Released: December 13, 2014 1:46 PM
* Made it so it goes dark when you use the bed and turns back to normal after mom's text ends.

### R27
* Released: December 13, 2014 3:27 PM
* Made the majority of the first cutscene (other than opening, so technically second cutscene). 
	* Tadukoo's mom will be in a thought bubble in the future.
* There may be text issues (in terms of placement).
* Tadukoo does not say his opening lines yet for the start of the bedroom.

### R28
* Released: December 13, 2014 3:52 PM
* Your mom's face is now in a thought bubble
* Your text is now centered correctly in the cutscene.

### R29
* Released: December 13, 2014 5:38 PM
* You can now skip the cutscene by pressing space at any point during it
* You may press s to skip one dialog at a time
* Resetting no longer makes you spasm and lying down 
* The right is blocked off by an invisible platform
* Each dialog appears for the same amount of time (unless skipped).

### R30
* Released: December 13, 2014 7:52 PM
* There are now two dialogs at the start of the bedroom level
* Added closet door to bedroom.

### R31
* Released: December 13, 2014 9:22 PM
* Closet door now opens
* There is a dialog about not needing to get dressed if interacting with the closet open.
* Introduced and found Issue # 7: Text is sometimes stored until a later point when skipping it.

### R32
* Released: December 13, 2014 11:01 PM
* Now there is a delay between opening the closet and trying to put clothes on
* The computer is in the room with two lines of dialog upon interaction.

### R33
* Released: December 14, 2014 9:17 AM
* Now when spasming, there is a picture of you sad in the upper right corner.

### R34
* Released: December 14, 2014 9:35 AM
* Added left facing player image.
* Can now start out left instead of right.
* Now change direction when walking.
* This version did not change its version number in the game.

### R35
* Released: December 14, 2014 12:52 PM
* Now spasm is animated to the left as well as right.

### R36
* Released: December 14, 2014 2:46 PM
* Now all current player graphics are double sided
* Player graphics are now stored in separate folders for left and right.
