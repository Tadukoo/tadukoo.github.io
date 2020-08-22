---
title: Tadukoo Bible Changelog
project: TadukooBible
index: 3
---
You can see what changes were made to each file on [the GitHub commits page](https://github.com/Tadukoo/TadukooBibleProject/commits/master).

#### Table of Contents
* [1.1 BETA 1 (June 30, 2016)](#11-beta-1-june-30-2016)
* [1.0.1 (October 26, 2015)](#101-october-26-2015)
* [1.0 (November 28, 2014)](#10-november-28-2014)

## 1.1 BETA 1 (June 30, 2016)

### Translations Added
* None this time.

### Command Changes
* ```/bible previous```
	* Usage is now ```/bible previous [type] [translation]```
		* Type is for verse, chapter, or book.
		* Type will go back by that type rather than the default verse.
		* Verse type goes back one verse no matter what (unless the translation is missing a previous book).
		* Chapter type goes back to the beginning of the chapter if the verse isn't the first one, otherwise the previous chapter.
		* Book type goes back to the beginning of the book if the chapter or verse isn't the first one, otherwise the previous book.
* ```/bible getbook```
	* ```/bible getbook previous``` now goes back by Minecraft book by default.
		* E.g. Exodus Book 1 to Genesis Book 17.
	* Can now do ```"previous:part"``` or ```"previous:book"```
		* Part goes back by Minecraft book.
		* Book goes back by Bible book.
		* Book will go back to Book 1 of a Bible book, unless Book 1 was the last book.
	* Can now do ```"next:part"``` or ```"next:book"```
		* Part goes forward by Minecraft book.
		* Book goes forward by Bible book.
* ```/bible statistics [player|top] [statistic]```
	* Added, can view your own statistics.
* ```/bible translation```
	* OEB is now listed.

### Permission Changes
* TadukooBible.translation.*
	* Added TadukooBible.translation.OEB.
* Added TadukooBible.translation.OEB
	* Allows you to use the OEB.
	* Default: true
* Added TadukooBible.statistics.*
	* Children: TadukooBible.statistics.use, TadukooBible.statistics.others, and TadukooBible.statistics.top
* Added TadukooBible.statistics.use
	* Allows you to use ```/bible statistics```
	* Default: true
* Added TadukooBible.statistics.others
	* Allows you to use ```/bible statistics [player]``` for other players' statistics.
	* Default: op
* Added TadukooBible.statistics.top
	* Allows you to use ```/bible statistics top <statistic>``` to view top statistics.
	* Default: op

### Configuration Changes
* Added OEB to translation settings.
	* Enables or disables OEB.
	* Default: True
* Added statistics.plugin
	* Enables or disables keeping track of server-wide statistics.
	* Default: True
* Added statistics.player.enabled
	* Enables keeping track of statistics per player.
	* Default: true
* Added auto-announce section
	* Contains: enabled, randomize-list, delay, and verses list.
	* enabled is default false, enables or disables the auto-announcing.
	* randomize-list is default false, randomizes the list of verses.
	* delay is the delay between verse announcements in minutes.
	* verses is a list of verses, which can contain "random" to do a random verse.
* Players.yml
	* Now contains statistics per player.
* Statistics.yml added
	* Contains server-wide statistics.
* Statistics included are:
	* verses-requested (verses read through /bible read, previous, next, last, or favorite)
	* verses-received (verses got from /bible send, this statistic is not included in statistics.yml)
	* verses-sent (verses sent using /bible send)
	* verses-favorited (verses favorited using /bible favorite)
	* verses-announced (verses broadcasted using /bible announce)
	* books-requested (books got from /bible getbook)
	* books-received (books received from /bible sendbook, this statistic is not included in statistics.yml)
	* books-sent (books sent using /bible sendbook)

### TBB Changes
* None this time.

### Other Changes
* Added EnumAvail
	* Has books that list whether incomplete translations have them or not.
* Changed alias strings in EnumCmd to String array, simplifying the class.
* Added some functionality for working with TadukooCore.
* Added basics for TadukooBibleBooks and this communicating with each other.
* Made other changes to improve plugin overall.

## 1.0.1 (October 26, 2015)

### Other Changes
* Fixed an issue where the plugin would fail to load.

## 1.0 (November 28, 2014)

### Books Added
* Isaiah
* Jeremiah
* Lamentations
* Ezekiel
* Daniel
* Hosea
* Joel
* Amos
* Obadiah
* Jonah
* Micah
* Nahum
* Habakkuk
* Zephaniah
* Haggai
* Zechariah
* Malachi

### Command Changes
* ```/b```
	* Now you can use ```/b``` instead of ```/bible``` for all ```/bible``` commands.
* ```/bible```
	* Now arguments may be typed in any order.
	* Read or aliases can only be first though.
	* Checks if player has translation permission.
* ```/bible send```
	* Now arguments may be typed in any order.
	* Now you may type aliases for anonymous.
	* Now can use bypass to bypass players.yml settings.
	* Now checks players.yml for if player has opted out of receiving verses or if sender is blocked by player.
* ```/bible previous```
	* Now goes back by verse rather than verse, chapter, or book.
* ```/bible previous, next, and last```
	* Now use Verse class to check stuff.
* ```/bible favorite```
	* Allows you to favorite a Bible verse.
	* Allows you to list favorite Bible verses.
* ```/bible random, getbook, sendbook, and announce```
	* Now you can type the arguments in any order.
* ```/bible getbook```
	* Added aliases getb and bget.
* ```/bible sendbook```
	* Added aliases sendb, bsend, giveb, and bgive.
	* Now you may type aliases for anonymous.
* ```/bible permission```
	* Aliases: perm and perms
	* Lists permissions or shows info about a permission.
	* Requires permission: TadukooBible.info.permission
* ```/bible read```, ```send```, and ```announce```
	* You can now use ```"favorite:#"``` or ```"favorite #"``` instead of a reference.
* ```/apocrypha```
	* Basic functionality set-up.
	* Always gives message about not being available yet.
* ```/apocrypha help```
	* Shows that no commands are available yet.
* ```/t```
	* Can do ```/t b``` or ```/t bible``` for same functionality as ```/bible```
	* Can do ```/t a``` or ```/t apocrypha``` for same functionality as ```/apocrypha```
	* ```/t``` will be standard for all Tadukoo plugins.
	* If another Tadukoo plugin is on the server, Tadukoo bible no longer controls ```/t```
	* If Tadukoo Core is on the server, it controls ```/t``` and the same functionality is available.

### Permission Changes
* Changed TadukooBible.*
	* Now gives:
		* TadukooBible.bible.*
		* TadukooBible.apocrypha.*
		* TadukooBible.debug
* Added TadukooBible.bible.*
	* Gives all bible permissions.
* TadukooBible.verse.*
	* Added TadukooBible.verse.favorite to children.
* Added TadukooBible.block.*
	* Gives all block permissions.
* Added TadukooBible.bypass.*
	* Gives all bypass permissions.
* Added TadukooBible.apocrypha.*
	* Gives all apocrypha permissions.
* Added TadukooBible.translation.*
	* Gives all translation permissions (default and KJV)
* Added TadukooBible.translation.default
	* Allows you to use the default translation. Overrides the translation's permission.
	* Default: true
* Added TadukooBible.translation.KJV
	* Allows you to use the KJV.
	* Default: true
* Added TadukooBible.verse.favorite
	* Allows use of /bible favorite.
	* Default: true
* Added TadukooBible.block.view
	* Allows using /bible block to view current information.
	* Default: true
* Added TadukooBible.block.verse
	* Allows using /bible block verse.
	* Default: true
* Added TadukooBible.block.book
	* Allows using /bible block book.
	* Default: true
* Added TaudkooBible.block.immune
	* Makes you immune from being blocked with /bible block.
	* Default: op
* Added TadukooBible.receive
	* Allows use of /bible receive.
	* Default: true
* Added TadukooBible.bypass.verse
	* Allows you to bypass players.yml verse settings.
	* Default: op
* Added TadukooBible.bypass.book
	* Allows you to bypass players.yml book settings.
	* Default: op
* Added TadukooBible.apocrypha.use
	* Allows use of /apocrypha.
	* Default: true
* Added TadukooBible.apocrypha.info.help
	* Allows use of /apocrypha help.
	* Default: true
* Added TadukooBible.debug
	* Shows you debug messages.
	* Default: false

### Configuration Changes
* Config.yml Changes
	* language setting added
		* Changes to en_US if "English" or "en" are there on startup.
		* Changes to en_US if it isn't already.
			* This will be used in the future to default it to en_US if a non-existant name is typed.
	* Removed PlayerRecords
		* This means player records are always kept.
		* This makes it so that all commands that require player records will always work.
	* Added statistics.player and statistics.plugin
		* player is for statistics per player.
		* plugin is for statistics for everyone.
	* Added debug
		* Shows debug info to console if set to true.
	* Renamed DefaultTranslation, DefaultBook, DefaultChapter, DefaultVerse, and DefaultPart to ```default.<type>```
	* Renamed Version to version.
	* Renamed Permissions to permissions.
	* Renamed Books to books.
* Languages File made
	* Added book descriptions from before.
	* Added translation description.
	* Added alias messages. (book and translation)
	* Added help pages.
* playerList.yml made
	* This lists player names and their UUIDs, used for commands where you type a player's name/UUID.

### Tadukoo Bible Books (TBB) Changes
* Made minor changes so it still works with Tadukoo Bible 1.0.

### Other Changes
* Made some changes to allow TadukooCore to work with it.
* ConfigCheck class made to check config.yml, rather than having function in the TB class.
* EnumAvail Made
	* Will be used in the future for when a translation is incomplete.
* EnumBooks Changes
	* Removed book descriptions and alias messages.
	* Removed alias3 (unused)
	* Moved book number to beginning for less confusion.
	* Removed num stuff, using ordinal() method instead.
	* Removed availability.
* EnumChps Changes
	* Removed switchChp, use fromString instead.
	* Added comments to this too.
* EnumCmds Changes
	* Added items for future commands.
	* Added setting for apocrypha (availability in /apocrypha)
	* Added anonymous for use in ```/bible send``` and ```/bible sendbook```.
		* Makes it so aliases may be typed.
* EnumHelp Changes
	* Put minor page number in here.
	* Put max boolean to use for getting maximum "minor" page.
	* Put title in there to get from language file.
	* Put paths in there to get from language file.
	* Changed it so that a max of 5 aliases can be listed per item.
* EnumPerms Changes
	* Added new permissions.
	* Description and children are now stored in language file.
* EnumTrans Changes
	* Removed translation description.
	* Removed alias message.
* permChecks Changes
	* Added type String for bible or apocrypha.
* Package changes
	* cmdhandling package renamed to commands.handling
	* "args" package renamed to commands.args
	* Apocrypha args package named commands.apocrypha.args
	* commands package will be used for dealing with the arguments after they're sorted out in the args package.
	* com.gmail.lucario77777777 renamed to com.gmail.realtadukoo
	
### Known Issues
* ```/bible help``` page 11 is too long.
* ```/bible help``` has pages with things like ```{defBook}```.
