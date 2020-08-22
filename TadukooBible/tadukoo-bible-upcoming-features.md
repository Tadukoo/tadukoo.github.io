---
title: Tadukoo Bible Upcoming Features
category: TadukooBible
---
This is about upcoming/planned features for [Tadukoo Bible](/projects/TadukooBible.html).

## Note
Please note all changes listed for upcoming versions are tentative. This means that they could get pushed back to a later version or even removed entirely. 
Even changes listed under "Eventual Features/Commands" could be removed or moved into the next version without notice.

If a feature says "(Done)" after it, it has already been completed for the upcoming version it is listed under. If an upcoming version has a lot of features, 
it may have a subsection for completed features, because Tadukoo uses this page as a checklist and that makes it easier sometimes.

> **Note:** (Note within a note?) Tadukoo Bible is currently on hiatus. Sometime in the near future I'm planning to rework the plans moving forward for this.

## 2.0
Tentative Deadline: TBD

The main change is that Tadukoo Bible will be able to be used for so much more than simply Bukkit. Over the next several days, this page will be edited to reflect the plans for the upcoming version.

### Translation Changes
Add Open English Bible

Add translations from biblehub.com (Done)
* This includes KJV, NIV, and 20 others. (Done)

### Command Changes
```/bible get <book> <chapter> <verse> <translation>```
* This is the official format for getting a verse, but the former ```/bible read``` command will go to this command anyway.

```/bible downloadtran <translation>``` (Done)
* Used by admins to download an entire translation of the Bible.
* This takes about 17 minutes for me, but would vary by your setup.
* Note: Verses are automatically downloaded and saved now when using the ```/bible get``` command.

### Other Changes
Make it so that additional translations may be downloaded from biblehub.com as needed. (Done)
* By default, verses are only downloaded when they are needed (and saved by default, but this can be configured to false).
* Can configure whether this is enabled or not.
* Include KJV in download, but have other translations as requiring looking up or downloading. (Done)

The content of Tadukoo Bible Books is now in this. (Done)
* This involves generating the files used for getting the Bible as Minecraft books. (Done)

## 1.1 Beta 2 (Partial Translations Capability and Some Fixes/Improvements)
Tentative Deadline: Unknown (canceled? - ideas will be transferred to another version)

### Command Changes
```/bible previous/next``` and other commands with previous/next in them (other than ```/bible getbook``` and ```/bible previous```)
* Make it so you can go back/forward by greater amounts optionally (book/chapter) (other than ```/bible getbook``` and ```/bible previous```)

```/bible info [permission]``` and ```/bible permission```
* Make it so you can do command aliases.

```/bible help```
* Add ```/bible previous [type]``` stuff.
* ```/bible getbook```
	* ```/bible getbook previous``` defaults to going back by Minecraft book.
	* ```/bible getbook previous:part``` and ```previous:book```
	* ```/bible getbook next:part``` and ```next:book```
* Add ```/bible statistics```
* Add examples
* page 11 (```/bible send```) is too long (due to alternate usage)
* Some pages have ```{defBook}``` and such instead of the default.book set in the config.
* Add possibility of random translation where it can be done.
* ```/bible announce [previous|next|last]```
* ```/bible statistics```
* Make it so ```/bible help``` stuff is simply generated from EnumHelp when the command is typed?

```/bible statistics top [statistic]```
* Can use top to see a chart of top players.
* A way to disable their statistics tracking.
* A permission to allow them to disable statistics tracking.
* Requires permission: TadukooBible.statistics.others to view statistics of others.
* Requires permission: TadukooBible.statistics.top to view charts.

```/bible books [book]```
* Improve the messages for the book descriptions?
* Add a list of translations where a book does/doesn't exist.
	* Add option for why if it doesn't exist.

```/bible translation [translation]```
* Improve the messages for the translation descriptions?
* List books that aren't available for translations (if there are any)
* Add good description for OEB.

```/bible config```
* Make it so that you can see what each setting does.
* Make an EnumSettings?

```/bible announce```
* Make it so you can type previous, next, or last instead of the reference.

Any command where you type a Bible book.
* If the book doesn't exist, add a new message per translation on why it doesn't exist.
* Check EnumTrans for translation completeness, if not complete, check EnumAvail then.

Make it so that translations can be random?
* This would add the random option to more commands.
* Make it so that someone can either type random (or its aliases) or specify what is random (e.g. randomverse or randombook)

### Permissions Changes
TadukooBible.statistics.top
* Allows using ```/bible statistics``` to view the statistics charts.
* Default: op

### Configuration Changes
Config.yml
* statistics.player.can-disable
	* Enables/disables letting players disable keeping track of their personal plugin usage statistics.
	* Default: false

* For random auto-announcing, verses can be set as more frequent than others?

### Other Changes
Finish Language file

Add debugging stuff to all commands.
* With debug permission and with debug config option.

Add comments and remove magic numbers.
* These are good programming practices that I followed near the beginning but stopped for some reason.
* They help to make it easier to understand the code (for me and if anyone would be helping me).

## 1.1 Beta 3 (Blocking and Special Books)
Tentative Deadline: Unknown (canceled? - ideas will be transferred to another version)

### Command Changes
```
/bible getbook "special" <start book> <start chapter> <start verse> 
                         [end book] [end chapter] <end verse>
/bible getbook "special" <start book> <start chapter> <end chapter>
```
* Also with ```/bible sendbook```.
* Allows you to select what verses go into a book to send to someone.
* Requires Tadukoo Bible Books plugin to use.
* Possibility to do ```<start book> <start chapter:start verse> <end chapter:end verse>, <start chapter:start verse> <end chapter:end verse>,...```
* Possibility to do ```<start book> <start chapter:start verse> - <end chapter:end verse>```
* Possibility to set a title?
* Saves configuration for various books as "Special#" so that ```/bible getbook "special" #``` may be typed.
* Make aliases for special.
* Also do with ```/bible sendbook```
* Perhaps ```/bible makebook``` to create the special books?
* Perhaps ```/bible getbook "special" #``` for user created books and have actual names for given books?

```/bible help```
* Add new information
** Add ```/bible block```
** Add ```/bible receive```

```/bible block <player> ["verse"|"book"|"special"|"all"]```
* Alias: ban
* Blocks a player from sending verses, books, special books, or all of the above to you.
* Leaving out ```"verse"|"book"|"special"|"all"``` will show the current settings.
* Sets in the players.yml in string list player.blocked.verse, player.blocked.book, and/or player.blocked.special.
* Requires TadukooBible.block.view to view current settings or use at all.
* Requires permission TadukooBible.block.verse, TadukooBible.block.book, TadukooBible.block.special, or TadukooBible.block.*
* Can have permission TadukooBible.block.immune so you can't be blocked.

```/bible receive ["verse"|"book"|"special"|"all"] ["true"|"false"]```
* Aliases: No aliases.
* Lets a player decide whether they want to receive books, special books, and verses or not.
	* This alters the players.yml file to set receive.book, receive.verse, and/or receive.special.
* Leaving out ```"true"|"false"``` will show what it is set to, while putting it in will set it.
* Leaving out ```"verse"|"book"|"special"|"all"``` will show the settings for all of them.
* Requires permission TadukooBible.receive

### Permission Changes
TadukooBible.book.*
* Add TadukooBible.book.get.special
* Add TadukooBible.book.send.special

TadukooBible.book.get.special
* Allows use of ```/bible getbook "special"```
* Default: true

TadukooBible.book.send.special
* Allows use of ```/bible sendbook "special"```
* Default: op

TadukooBible.block.*
* Add TadukooBible.block.special

TadukooBible.block.special
* Allows you to use ```/bible block <player> <"special">```
* Default: true

### Configuration Changes
Config.yml
* special-books
	* Allows special books through ```/bible getbook``` and ```sendbook```.
	* Default: false
	* Will set to false on startup if Tadukoo Bible Books is not present.

Players.yml
* player.receive.special
	* Decides whether you receive special books or not.
	* Set through ```/bible receive```.
	* player.receive.book overrides this.
* ```player.blocked.<player>.special```
	* Allows you to define players who are blocked from sending you special books.
	* Set through ```/bible block```.
* ```player.blocked.<player>.both```
	* Change to ```player.blocked.<player>.all```

### TBB Changes
Make it so that special ranges can be made into a book.
* Used for ```/bible getbook "special"```

## 1.2
Tentative Deadline: Unknown (canceled? - ideas will be transferred to another version)

### Other Changes
Add partial stuff for EnumAvail
* The #'s in "Partial#:#" are used for what ordinal the translation is and what setting in the translation is used for that book, respectively.

## Eventual Features/Commands

### Books to Add
Maybe add the Apocrypha (a.k.a. Deuterocanonical books) with a warning that they aren't inspired?
* Even though I don't believe the books in the Apocrypha, I like to look at them because they're interesting to me.
* I'm interested in looking at beliefs I believe are wrong to figure out why they're wrong.
* Add permissions for the apocrypha in general as well as per book.

Add books that contain verses about specific topics (or perhaps commentaries?)

Add testimonies?
* Do through ```/bible getbook```

### Translations to Add
Need permission for some.
* Ask about New American Standard Bible (NASB) ?
* Ask about Revised Standard Version (RSV) ?

Some are public domain.
* American Standard Version (ASV) ?

### Command Changes
Make it so command blocks (and maybe unknown senders?) can use the commands.

```/bible getbook "special" <topic>```
* Use this command for books that contain verses about specific topics if they're added (e.g. ```/bible getbook "special" "Marriage"``` for a book with verses about
marriage)

```/bible dictionary [page|word]```
* Allows you to look up words (list them or view their definition)

```
/bible YouTube [translation|topic|person]
/bible YouTube [book] [chapter] [verse]
```
* Gives links to YouTube videos about specific verses/people/topics in the Bible.

```/apocrypha```
* For viewing the apocrypha, has (mostly?) the same commands as ```/bible```.
* See above for note with apocrypha (under book changes)

### Permission Changes
Permissions for use with ```/apocrypha```.

### Configuration Changes
Enable or disable the apocrypha or certain books in it.

Make it so that on joining, a player's stuff is set to the defaults in players.yml?

### Other Changes
Make it so that you can set it up to announce random Bible verses on the server.
* Config file options to enable and set interval.
* Config options to do completely random or designated verses list.

More languages. (These will at first just be translations of the information the plugin provides, then later have their own translations too.)
* Spanish?
* French?
* German?

After Bukkit releases a 1.8 build, possibly using clickEvent at the end of a book to get the next book.

## Suggest Features
If you have a feature/command/alias to suggest, please use either BukkitDev's Ticket System or GitHub's Issue Tracker and label it as an Enhancement.
