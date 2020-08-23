---
title: Tadukoo Essentials Changelog
project: TadukooEssentials
index: 1
---

#### Table of Contents
* [Alpha 0.0.1](#alpha-001)
* [Alpha 0.0.2](#alpha-002)
* [Alpha 0.0.3](#alpha-003)
* [Alpha 0.0.3.1](#alpha-0031)
* [Alpha 0.0.3.2](#alpha-0032)
* [Alpha 0.0.3.3](#alpha-0033)
* [Alpha 0.0.3.4](#alpha-0034)
* [Alpha 0.0.3.5](#alpha-0035)
* [Alpha 0.0.3.6](#alpha-0036)
* [Alpha 0.0.3.7](#alpha-0037)
* [Alpha 0.0.4](#alpha-004)
* [Alpha 0.0.5](#alpha-005)
* [Alpha 0.0.5.1](#alpha-0051)
* [Alpha 0.0.5.2](#alpha-0052)
* [Alpha 0.0.5.3](#alpha-0053)
* [Alpha 0.0.5.4](#alpha-0054)
* [Alpha 0.0.6](#alpha-006)
* [Alpha 0.0.6.1](#alpha-0061)
* [Alpha 0.0.7](#alpha-007)
* [Alpha 0.0.7.1](#alpha-0071)
* [Alpha 0.0.7.3](#alpha-0073)
* [Alpha 0.0.7.3.1](#alpha-00731)
* [Alpha 0.0.7.4](#alpha-0074)
* [Alpha 0.0.7.5](#alpha-0075)
* [Alpha 0.0.7.6](#alpha-0076)
* [Alpha 0.0.7.7](#alpha-0077)
* [Alpha 0.0.7.8](#alpha-0078)
* [Alpha 0.0.8.0](#alpha-0080)
* [Alpha 0.0.8.1](#alpha-0081)
* [Alpha 0.0.8.2](#alpha-0082)
* [Alpha 0.0.8.3](#alpha-0083)
* [Alpha 0.0.8.4](#alpha-0084)
* [Alpha 0.0.8.5](#alpha-0085)
* [Alpha 0.0.8.6](#alpha-0086)
* [Alpha 0.0.8.7](#alpha-0087)
* [Alpha 0.0.8.8](#alpha-0088)
* [Alpha 0.0.8.9](#alpha-0089)
* [Alpha 0.0.9.0](#alpha-0090)
* [Alpha 0.0.9.1](#alpha-0091)
* [Alpha 0.0.9.2](#alpha-0092)
* [Alpha 0.0.9.3](#alpha-0093)
* [Alpha 0.0.9.4](#alpha-0094)
* [Alpha 0.0.9.5](#alpha-0095)
* [Alpha 0.0.9.6](#alpha-0096)
* [Alpha 0.1](#alpha-01)
* [Alpha 0.1.0.1](#alpha-0101)
* [Alpha 0.1.0.2](#alpha-0102)
* [Alpha 0.1.0.3](#alpha-0103)
* [Alpha 0.1.0.4](#alpha-0104)
* [Alpha 0.1.0.5](#alpha-0105)
* [Alpha 0.1.0.6](#alpha-0106)
* [Alpha 0.1.0.7](#alpha-0107)
* [Alpha 0.1.0.8](#alpha-0108)
* [Alpha 0.1.0.9](#alpha-0109)
* [Alpha 0.1.1.0](#alpha-0110)
* [Alpha 0.1.1.1](#alpha-0111)
* [Alpha 0.1.1.2](#alpha-0112)
* [Alpha 0.1.1.3](#alpha-0113)
* [Alpha 0.1.1.4](#alpha-0114)
* [Alpha 0.1.1.5](#alpha-0115)
* [Alpha 0.1.1.6](#alpha-0116)
* [Alpha 0.2](#alpha-02)

## Alpha 0.0.1
* First version
* Command ```/basic``` Added
	* Does nothing, can be used by console and player.

## Alpha 0.0.2
* Command ```/basic2``` Added
	* Does nothing, can only be used by a player.

## Alpha 0.0.3
* Moved commands to a separate class.
* KNOWN BUG: ```/basic2``` doesn't work correctly.

## Alpha 0.0.3.1
* Tried to fix ```/basic2```
* KNOWN BUG: ```/basic2``` is not fixed.

## Alpha 0.0.3.2
* Bug Fix:
	* ```/basic2``` is fixed.

## Alpha 0.0.3.3
* Experimenting with different syntax for ```/basic2```.
* KNOWN BUG: There are mistakes in ```/basic2```.

## Alpha 0.0.3.4
* Bug Fix:
	* ```/basic2``` is fixed.

## Alpha 0.0.3.5
* Added defaults for permissions of ```/basic``` and ```/basic2```
	* ```/basic=true```
	* ```/basic2=op```
* KNOWN BUG: Plugin fails to load.

## Alpha 0.0.3.6
* Bug Fix:
	* Plugin now loads.
		* The permission defaults were under the commands by mistake.
* KNOWN BUG:
	* Permissions don't work right.

## Alpha 0.0.3.7
* Bug Fix:
	* Fixed permissions.
		* Permissions had ```<Plugin name>``` at the beginning in the commands section by mistake.

## Alpha 0.0.4
* Added ```/sendme``` command.
	* Sends "Sent" (in gold) to the player.

## Alpha 0.0.5
* Removed ```/sendme``` command.
* Added ```/heal``` command
	* Heals a player.
		* Also added ```/h``` alias.
* KNOWN BUG:
	* ```/h``` doesn't work.

## Alpha 0.0.5.1
* Added error message to commands if a player is offline.
* KNOWN BUG:
	* ```/h``` doesn't work.

## Alpha 0.0.5.2
* Now ```/heal``` or ```/h``` will stop the player from burning as well.
* KNOWN BUG:
	* ```/h``` doesn't work.

## Alpha 0.0.5.3
* Now ```/heal``` will send a message to the healed player saying "You have been healed by nameOfPersonWhoHealedYou!"
* KNOWN BUG:
	* ```/h``` doesn't work.
	* ```/heal``` will send "You have been healed by CraftPlayer (name = nameOfPersonWhoHealedYou)".

## Alpha 0.0.5.4
* Bug Fix:
	* ```/heal``` will send "You have been healed by CraftPlayer (name = nameOfPersonWhoHealedYou)".
		* Now it will send "You have been healed!"

## Alpha 0.0.6
* ```/heal``` Removed.
* ```/tport``` Added.
	* Teleports a player to another player.
* Bug Fix:
	* ```/h``` doesn't work.
		* ```/h``` Removed.

## Alpha 0.0.6.1
* ```/tport``` moved to CommandExecutor file.
	* It was in the main file.

## Alpha 0.0.7
* Re-added ```/heal```.
	* This time the alias ```/h``` isn't included.

## Alpha 0.0.7.1
* Added permissions and usage for ```/heal``` and ```/tport```.

## Alpha 0.0.7.3
* Added ```/kill``` and permissions and usage for it.
* Update Number Note:
	* After this usage and permissions only count for the number if it wasn't included immediately.

## Alpha 0.0.7.3.1
* Fixed a simple mistake in the plugin.yml.
* Update Number Note:
	* No version after this one will have a fifth decimal place.
* KNOWN BUG:
	* Commands don't work.

## Alpha 0.0.7.4
* Bug Fix:
	* Commands don't work.
		* Fix didn't work.
* KNOWN BUG:
	* Commands don't work.

## Alpha 0.0.7.5
* Bug Fix:
	* Commands don't work.
		* Apparently I was using the string instead of the command itself?
			* Nope, didn't fix it.
* KNOWN BUGS:
	* Commands don't work.

## Alpha 0.0.7.6
* Unknown
* KNOWN BUG:
	* Commands don't work.

## Alpha 0.0.7.7
* Bug Fix:
	* Commands don't work.
		* Fixed mistake with commands.
		* I had used the command type instead of the string type, so it didn't know what I meant.
* KNOWN BUGS:
	* Typing a correct command sometimes shows the command usage.
	* If a player is offline, it won't show the error message.

## Alpha 0.0.7.8
* Bug Fixes:
	* Typing a correct command sometimes shows the command usage.
		* No longer shows.
	* If a player is offline, it won't show the error message.
		* Error message is now displayed.

## Alpha 0.0.8.0
* Now TNT and Bedrock disappear when placed.
	* The player will say through the chat "I just placed < TNT/BEDROCK >!"

## Alpha 0.0.8.1
* If you type heal in chat, you will be healed.
* If you type kill in chat, you will die.

## Alpha 0.0.8.2
* Added ```/flip```.
	* Flips a coin.
* KNOWN BUG:
	* ```/flip``` doesn't work.

## Alpha 0.0.8.3
* Added ```/feed```.
* Added ```/starve```.
* Bug Fix:
	* ```/flip``` doesn't work.
		* Removed ```/flip```.

## Alpha 0.0.8.4
* Added ```/suicide```.
* Added ```/thelp```.
	* Shows help for Tadukoo Plugin commands.

## Alpha 0.0.8.5
* Added ```/ping```
	* Says "Pong!" to the user, if the user is a player.
* Removed ```/basic```.
* Removed ```/basic2```.
* KNOWN BUGS:
	* Console can't use commands.
	* ```/suicide``` doesn't work correctly.

## Alpha 0.0.8.6
* Bug Fixes:
	* Console can't use commands.
		* Still broken, but attempted fix.
	* ```/suicide``` doesn't work correctly.
		* Now ```/suicide``` does work correctly.
* KNOWN BUG:
	* Console can't use commands.

## Alpha 0.0.8.7
* Bug Fix:
	* Console can't use commands.
		* Now certain commands can be used through the console.
* KNOWN BUG:
	* Console would get the usage message after typing certain commands correctly.

## Alpha 0.0.8.8
* Bug Fix:
	* Console would get the usage message after typing certain commands correctly.
		* Messages are gone now.

## Alpha 0.0.8.9
* Renamed tadukoopluginmain to Main.
* Renamed MyBlockListener to BlockListener.
* Renamed MyPlayerListener to PlayerListener.
* Renamed TadukooPluginCommandExecutor to MainCommandExecutor.
* Basically the classes have more logical names; there is no known performance change).

## Alpha 0.0.9.0
* Added ```/gamemode```.
	* Also alias ```/gm```.
	* Also alias ```/gmt```.

## Alpha 0.0.9.1
* Added a, c, and s as possible parameters in ```/gamemode```.

## Alpha 0.0.9.2
* Added ```/adventure```.
	* Also alias ```/gma```.
	* Sets a player's gamemode to adventure.
* Added ```/creative```.
	* Also alias ```/gmc```.
	* Sets a player's gamemode to creative.
* Added ```/survival```.
	* Also alias ```/gms```.
	* Sets a player's gamemode to survival.

## Alpha 0.0.9.3
* Added ```/fly```
	* Sets flight on or off for a player.

## Alpha 0.0.9.4
* Each player is sent a message when joining the server.

## Alpha 0.0.9.5
* Added ```/killall```.
	* Kills all players on the server.
* Added ```/motd```.
	* Displays the motd, which is configurable in the config.yml.

## Alpha 0.0.9.6
* Moved MainCommandExecutor to a new commands package.

## Alpha 0.1
* Moved Commands to separate classes.
* Made it so ```/ping``` can be set on or off in config.yml.
* KNOWN BUGS:
	* Can't use any commands except ```/ping```.
	* Players don't get the motd upon joining.

## Alpha 0.1.0.1
* Bug Fix:
	* Can't use any commands except ```/ping```.
		* Now you can use all of them again.
* KNOWN BUGS:
	* Players don't get the motd upon joining.

## Alpha 0.1.0.2
* Added ```/setwarp```
	* Sets a warp, but there's no command to teleport to it.
* KNOWN BUGS:
	* Players don't get the motd upon joining.
	* ```/setwarp``` doesn't work.

## Alpha 0.1.0.3
* Bug Fix:
	* ```/setwarp``` doesn't work.
		* Temporarily disabled.
	* Players don't get the motd upon joining.
		* Temporarily disabled.

## Alpha 0.1.0.4
* Added ```/time```
	* Sets the time to day or night.

## Alpha 0.1.0.5
* Added ```/timer```
	* Counts down from 3, then says "GO!".

## Alpha 0.1.0.6
* Re-enabled Player join motd.
* KNOWN BUG:
	* Player join motd doesn't work.

## Alpha 0.1.0.7
* Added Color Codes.
* Bug Fix:
	* Player join motd doesn't work.
		* Re-disabled Player join motd.
* KNOWN BUG:
	* Color codes don't work.

## Alpha 0.1.0.8
* Changed enabled and disabled messages a bit.

## Alpha 0.1.0.9
* Added ```/day```
	* Sets the time to day.
* Added ```/night```
	* Sets the time to night.
* ```/time day``` improved
	* Now sets the time to 0 instead of 12000.

## Alpha 0.1.1.0
* Re-added plugin enable and disable messages.
* Re-added player join motd.
* KNOWN BUG:
	* Player join motd gives an error and doesn't work.

## Alpha 0.1.1.1
* ```/setwarp``` and ```/warp``` added.
* BUG FIX:
	* Player join motd gives an error and doesn't work.
		* Temporarily disabled.

## Alpha 0.1.1.2
* ```/delwarp``` added.

## Alpha 0.1.1.3
* Added ```/sun```

## Alpha 0.1.1.4
* Reorganized commands and permissions.
* Created the commands.yml file.
* Minor code cleanup.

## Alpha 0.1.1.5
* Renamed ```/timer``` to ```/countdown```
* Renamed ```/tport``` to ```/tp```
* Permissions groups added.
	* Ex. Tadukooplugin.general.*

## Alpha 0.1.1.6
* Warps are now stored in warps.yml

## Alpha 0.2
* All commands can be set to true or false in the commands.yml file.
