---
title: Tadukoo Bible Beta Changelog
project: TadukooBible
index: 2
---
You can see what changes were made to each file on [the GitHub commits page](https://github.com/Tadukoo/TadukooBibleProject/commits/master).

#### Table of Contents
* [Beta 0.9 (October 4, 2014)](#beta-09-october-4-2014)
* [Beta 0.7 (September 20, 2014)](#beta-07-september-20-2014)
* [Beta 0.5 (September 1, 2014)](#beta-05-september-1-2014)
* [Beta 0.4 (August 17, 2014)](#beta-04-august-17-2014)
* [Beta 0.3 (July 31, 2014)](#beta-03-july-31-2014)
* [Beta 0.2 (July 19, 2014)](#beta-02-july-19-2014)

## Beta 0.9 (October 4, 2014)

### Books Added
* Joshua
* Judges
* Ruth
* 1 Samuel
* 2 Samuel
* 1 Kings
* 2 Kings
* 1 Chronicles
* 2 Chronicles
* Ezra
* Nehemiah
* Esther
* Job

### Tadukoo Bible Books (TBB) Changes
* List book now does not have new pages for each book.
	* This condenses it so that it fits into one list book.
	
## Beta 0.7 (September 20, 2014)

### Books Added
* 1 Thessalonians
* 2 Thessalonians
* 1 Timothy
* 2 Timothy
* Titus
* Philemon
* Hebrews
* James
* 1 Peter
* 2 Peter
* Ecclesiastes
* Song of Songs/Solomon

### Command Changes
* ```/bible books [book]```
	* Added new information for some books.
		* Joshua through Job.
		* Ecclesiastes and Song of Songs.
		* 1 Thessalonians through 2 Peter.

### Configuration Changes
* Added Version and startup-checks.
	* Both decide whether the config.yml will be checked.

## Beta 0.5 (September 1, 2014)

### Books Added
* Galatians
* Ephesians
* Philippians
* Colossians
* Jude
* Revelation

### Command Changes
* All commands that include a book can have spaces in the book name.

```/bible send```
* Now shows ```"[<from-player>-><to-player>]"``` before the verse.

```/bible getbook```
* ```/bible getbook list```
	* Gives you a book that lists all the available Minecraft books.
* ```/bible getbook random [translation]```
	*Gives you a random book.

```/bible sendbook```
* Now sends a message to the player receiving the book.
* ```/bible sendbook <player> <book> <part> "anonymous" [translation]```
	* Allows you to send a book anonymously to another player.

```/bible info```
* ```/bible info "permissions"```
	* Shows a list of permissions.
* ```/bible info [permission]```
	* Shows information about a permission.

```/bible books [book]```
* Now has new aliases.
* Genesis through Deuteronomy have updated information.
* Psalms and Proverbs have updated information.
* Matthew through 2 Corinthians have updated information.
* 1 through 3 John have updated information.
* Jude and Revelation have new information.
* Galatians through Colossians have new information.

```/bible translation [translation]```
* Now has new aliases.
* KJV has updated information.

```/bible help [page|command]```
* Updated to include new aliases for ```/bible translation```.
* Updated to include ```/bible info [permission|"permissions"]```.
* Updated to include ```/bible getbook list```.
* Updated to include ```/bible getbook random```.
* Updated to show that ```/bible sendbook``` now requires the book and part.
* Updated to include ```/bible send``` and ```/bible sendbook```'s anonymous option and permission.
* Updated to include ```/bible announce```'s ```<chapter:verse>``` option.
* Updated to include new aliases for ```/bible books```.

```/bible announce```
* Can now do ```<chapter:verse>``` rather than ```<chapter> <verse>```
* Now shows the reference in the broadcast.

### Permission Changes
TadukooBible.verse.send
* Default is now ops only.

TadukooBible.verse.receive
* Allows you to receive verses through /bible send.
* Default: true

TadukooBible.book.receive
* Allows you to receive books through /bible sendbook.
* Default: true

TadukooBible.anonymous.verse
* Allows you to send a verse to another player anonymously.
* Default: op

TadukooBible.anonymous.book
* Allows you to send a book to another player anonymously.
* Default: op

TadukooBible.anonymous.*
* Gives the two above permissions.

### Config Changes
None this version.

### Other changes (Usually just code)
* MainCommandExecutor was renamed to CommandsExec.
* Commands package renamed to cmdhandling.
* cmdhandling package now does general things, while the commands package does command specific things.
* Created package commands to handle the commands.
	* Includes Args class to handle general things.
	* Includes ```<Command>``` classes to handle command specific things.
* CMDRandom class renamed to Randomcmd.
* Randomize class created in cmdhandling to handle random things.
* Made EnumPerms to handle /info [permission].
* Updated Tadukoo Bible Books to v.1.0.
	* Now verse numbers are in bold with no space before the first word of a verse.
	* Now each book of the Bible has a separate file for its Minecraft books.
	* All books have been updated using this new version.

## Beta 0.4 (August 17, 2014)

### Books Added
* Proverbs
* Acts
* Romans
* 1 Corinthians
* 2 Corinthians

### Command Changes
* Now you can use spaces in book names for certain commands.
	* e.g. "1 John" rather than "1John" or "Song of Songs" rather than "SongofSongs"
* There are now more aliases (abbreviations) for the books of the Bible.
* ```/bible [book] [chapter #] [verse #] [translation]```
	* Can now use aliases: ```/bible [alias] [book] [chapter #] [verse #] [translation]```
		* Aliases: read, verseread, readverse, vread, and readv.
	* Can now type ```/bible [book] [chapter #:verse #] [translation]```
		* Works with aliases as well.
* ```/bible send <player> <book> <chapter> <verse> [translation]``` or ```/bible send <player> <book> <chapter:verse> [translation]```
	* Sends a verse to another player.
* ```/bible getbook```
	* Now next and previous skip books that are currently unavailable.
* ```/bible info [translation|book|"plugin"|"books"|"translations"] [page]```
	* Allows you to view plugin, book, or translation info or lists now.
* ```/bible plugin```
	* Shows plugin information.
* ```/bible books [book]```
	* Can now type a book for info about it.
* ```/bible translation [translation]```
	* Can now type a translation for info about it.
* ```/bible config <setting> [value]```
	* Using ```/bible config list``` to list all the settings has been updated to include the other settings.
* ```/bible <anything_that_isn't_a_command_or_book_of_the_Bible> [meaningless_parameters]```
	* Now tells you to type ```/bible help``` for help.

### Permission Changes
* Added TadukooBible.verse.send
	* Allows use of ```/bible send```.
* Added TadukooBible.info.plugin
	* Allows use of ```/bible plugin``` and using ```/bible info``` for plugin info.
* TadukooBible.info.book
	* Required to use ```/bible info``` for book info.
* TadukooBible.info.translation
	* Required to use ```/bible info``` for translation info.

### Config Changes
* Can now configure Default Book, Chapter, Verse, and Part.

### Other Changes (Usually just code)
* method sendToPlayer changed to sendVerseToPlayer and includes the reference.
	* Now also calls savepRecs rather than having everything call both methods by themselves.
* method sendInfoToPlayer made for use with ```/bible information <translation>```
* Now SONG is a "command" (Listed in EnumCmds like FIRST, SECOND, and THIRD, used for handling when a player includes spaces in certain book names).
	* Has not been checked yet, as Song of Songs is not available in this version yet. This may need improved or changed in the future.
* EnumBooks now includes more aliases.
* EnumBooks and EnumChps now have a default method.
* Book and translation information is now stored completely in EnumBooks and EnumTrans rather than in yml files.
* Lists package renamed to Info.
	* This package will include the information used with ```/bible help```, ```info```, ```plugin```, ```books```, and ```translations```.
* BooksList renamed to Books.
	* bookList method renamed to list.
	* This class will include information about books.
* isBook method changed to handle "1st", "2nd", "3rd", and "song" books. (e.g. 1 John, 2 John, 3 John, and Song of Songs)
	* This may have removed warnings about having to type a book name rather than typing just a 1, 2, 3, or song of.
* EnumTrans now includes an aliasList String for use with translation info.
* MainCommandExecutor now handles too many/not enough args issues and sorting out args for some commands.
* Added the extra bits in EnumChps to prepare for future books being added.
* Tadukoo Bible Books (a separate plugin I use to make the in game books)
	* Updated so that there isn't a blank line before a new chapter.
	* Be thankful I updated all the books, this currently takes between 6 and 15 seconds per chapter of the Bible.
		* With the current books, this equals out to about 1 hour 33 minutes 59 seconds.
	* Just imagine, I have to do this if I ever make changes to TadukooBibleBooks (the plugin I use to make the books).
		* I plan to update it for Beta 0.5 of this plugin, but I'll probably update it before I add the new books so that I don't have to do it all at once.

## Beta 0.3 (July 31, 2014)

### Books Added
* Psalms

### Command Changes
* Aliases for books are fixed for ```/bible getbook``` and ```/bible givebook```.
* Added ```/bible previous [translation]```
	* Aliases: pre, prev, back, before, and b4.
	* Shows you the Bible verse before the one you last read.
	* Gives a message if trying to go before Genesis 1:1.
	* Requires permission: TadukooBible.verse.previous
* Added ```/bible next [translation]```
	* Aliases: forward, for, after, aft, nextverse, versenext, nextv, and vnext.
	* Shows you the Bible verse after the one you last read.
	* Gives a message if trying to go after 3 John 1:14.
	* Requires permission: TadukooBible.verse.next
* Added ```/bible last [translation]```
	* Aliases: saved, save, load, lastverse, verselast, lastv, vlast, savedverse, savedverse, vsaved, savedv, vsave, versesave, loadverse, verseload, vload,
and loadv.
	* Shows you the Bible verse you last read.
	* Requires permission: TadukooBible.verse.last
* ```/bible givebook```
	* Command name changed to ```/bible sendbook```
	* Added aliases: sendbook, booksend, sendbible, and biblesend.
	* Permission changed to TadukooBible.book.send
* ```/bible help [page]```
	* Now uses EnumHelp for ```[page]```. This allows for more keywords and easier updates in the future.

### Permission Changes
* Added TadukooBible.*
	* Gives all permissions.
* Added TadukooBible.verse.previous
	* Allows use of ```/bible previous```
	* Default: true
* Added TadukooBible.verse.next
	* Allows use of ```/bible next```
	* Default: true
* Added TadukooBible.verse.last
	* Allows use of ```/bible last```
	* Default: true
* Added TadukooBible.book.send
	* Allows use of ```/bible sendbook```
	* Replaces TadukooBible.givebook
	* Default: op
* Added TadukooBible.book.get
	* Allows use of ```/bible getbook```
	* Replaces TadukooBible.getbook
	* Default: true
* Added TadukooBible.verse.read
	* Allows use of ```/bible [book] [chapter #] [verse #] [translation]```.
	* Default: true
* Added TadukooBible.verse.random
	* Allows use of ```/bible random```.
	* Replaces TadukooBible.random.
	* Default: true
* Added TadukooBible.verse.announceget
	* Allows you to receive broadcasts from ```/bible announce```.
	* Default: true
	* Replaces TadukooBible.announceget
* Added TadukooBible.info.help
	* Allows use of ```/bible info``` and ```/bible help```.
	* Replaces TadukooBible.help and TadukooBible.info.
* Added TadukooBible.info.book
	* Allows use of ```/bible books```
	* Replaces TadukooBible.books
* Added TadukooBible.info.translation
	* Allows use of ```/bible translations```
	* Replaces TadukooBible.translations
* Added TadukooBible.op.config
	* Allows use of ```/bible config```
	* Replaces TadukooBible.config
* Added TadukooBible.op.announce
	* Allows use of ```/bible announce```
	* Replaces TadukooBible.announce
* Added TadukooBible.*
	* Gives all permissions.
	* Gives use, verse.*, book.*, info.*, and op.*
* Added TadukooBible.verse.*
	* Gives all verse permissions.
	* Gives verse.read, previous, next, last, random, and announceget
* Added TadukooBible.book.*
	* Gives all book permissions.
	* Gives book.get and send
* Added TadukooBible.info.*
	* Gives all info permissions.
	* Gives info.help, book, and translation.
* Added TadukooBible.op.*
	* Gives all op permissions.
	* Gives op.config and announce.
* Removed TadukooBible.givebook
	* Replaced by TadukooBible.book.send
* Removed TadukooBible.getbook
	* Replaced by TadukooBible.book.get
* Removed TadukooBible.random
	* Replaced by TadukooBible.verse.random
* Removed TadukooBible.announceget
	* Replaced by TadukooBible.verse.announceget
* Removed TadukooBible.info
	* Replaced by TadukooBible.info.help
* Removed TadukooBible.help
	* Replaced by TadukooBible.info.help
* Removed TadukooBible.books
	* Replaced by TadukooBible.info.book
* Removed TadukooBible.translations
	* Replaced by TadukooBible.info.translation
* Removed TadukooBible.config
	* Replaced by TadukooBible.op.config
* Removed TadukooBible.announce
	* Replaced by TadukooBible.op.announce

### Other Changes
* Moved commands to separate classes for easier changes in the future.
* Using the "read" command (```/bible [book] [chapter] [verse] [translation]```) or ```/bible getbook``` now saves a record of last verse/book read (if PlayerRecords = true
in the config.yml).
* There is now an Enum for translations in preparation for future translations.
* ```/bible getbook previous|next|last``` now uses EnumCmds to check aliases.
* ```/bible getbook``` and ```/bible givebook``` now use EnumBooks to check for book names or aliases.
* MainCommandExecutor's tranCheck method now uses EnumTrans.
* MainCommandExecutor now handles common methods while command classes handle command-specific methods.
* ```<book>Info```, ```<book>Lim```, ```<book>#```, and ```<chapter>info``` are now in code instead of in config files.
* Added EnumHelp for use with ```/bible help```

## Beta 0.2 (July 19, 2014)
* Added John.
* Moved Enums to a separate package.
* Moved PermissionsChecker to Commands package.
* Improved some commands and fixed bugs found or created during development of version.
