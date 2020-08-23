---
title: Tadukoo Essentials Permissions Guide
blurb: How to use the permissions for the Tadukoo Essentials plugin.
project: TadukooEssentials
---
This guide explains the permissions for [Tadukoo Essentials](/projects/TadukooEssentials.html).

## Special Permissions
Tadukooplugin.*
* Gives access to all commands.
* Children:
	* Tadukooplugin.cheat.*: true
	* Tadukooplugin.general.*: true
	* Tadukooplugin.moderator.*: true
	* Tadukooplugin.teleport.*: true

Tadukooplugin.cheat.*
* Gives access to all cheating commands.
* Children:
	* Tadukooplugin.feed: true
	* Tadukooplugin.gamemode: true
	* Tadukooplugin.fly: true
	* Tadukooplugin.heal: true
	* Tadukooplugin.starve: true
	* Tadukooplugin.time: true

Tadukooplugin.general.*
* Gives access to all general commands.
* Children:
	* Tadukooplugin.motd: true
	* Tadukooplugin.suicide: true
	* Tadukooplugin.thelp: true

Tadukooplugin.moderator.*
* Gives access to all moderator commands.
* Children:
	* Tadukooplugin.countdown: true
	* Tadukooplugin.kill: true
	* Tadukooplugin.killall: true
	* Tadukooplugin.ping: true

Tadukooplugin.teleport.*
* Gives access to all teleportation commands.
* Children:
	* Tadukooplugin.tp: true
	* Tadukooplugin.warp.*: true

Tadukooplugin.gamemode
* Gives access to all gamemode commands.
* Children:
	* Tadukooplugin.adventure: true
	* Tadukooplugin.creative: true
	* Tadukooplugin.survival: true

Tadukooplugin.time
* Gives access to /time, /day, and /night
* Children:
	* Tadukooplugin.day: true
	* Tadukooplugin.night: true

Tadukooplugin.warp.*
* Gives access to all warp commands.
* Children:
	* Tadukooplugin.delwarp: true
	* Tadukooplugin.setwarp: true
	* Tadukooplugin.warp: true

## Normal Permissions
Tadukooplugin.adventure
* Gives access to /adventure and /gma
* Default: op

Tadukooplugin.countdown
* Gives access to /countdown
* Default: op

Tadukooplugin.creative
* Gives access to /creative and /gmc
* Default: op

Tadukooplugin.day
* Gives access to /day
* Default: op

Tadukooplugin.delwarp
* Gives access to /delwarp
* Default: op

Tadukooplugin.feed
* Gives access to /feed
* Default: op

Tadukooplugin.fly
* Gives access to /fly
* Default: op

Tadukooplugin.heal
* Gives access to /heal
* Default: op

Tadukooplugin.kill
* Gives access to /kill
* Default: op

Tadukooplugin.killall
* Gives access to /killall
* Default: op

Tadukooplugin.motd
* Gives access to /motd
* Default: true

Tadukooplugin.night
* Gives access to /night
* Default: op

Tadukooplugin.ping
* Gives access to /ping
* Default: true

Tadukooplugin.setwarp
* Gives access to /setwarp
* Default: op

Tadukooplugin.starve
* Gives access to /starve
* Default: op

Tadukooplugin.suicide
* Gives access to /suicide
* Default: true

Tadukooplugin.sun
* Gives access to /sun
* Default: op

Tadukooplugin.survival
* Gives access to /survival and /gms
* Default: op

Tadukooplugin.thelp
* Gives access to /thelp
* Default: true

Tadukooplugin.tp
* Gives access to /tp
* Default: op

Tadukooplugin.warp
* Gives access to /warp
* Default: true
