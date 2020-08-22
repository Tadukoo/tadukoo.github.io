---
title: Tadukoo Bible Commands Guide
blurb: How to use the commands for the Tadukoo Bible plugin.
project: TadukooBible
---
This guide explains the commands for [Tadukoo Bible](/projects/TadukooBible.html).

## Commands
### Key
* ```<Required Parameter>```
* ```[Optional Parameter]```
* ```[This Parameter|Or This Parameter]```
* ```<"Type exactly this">```
* ```["You could type exactly this"]```

### Notes
* Anywhere a book name can be typed, you can include spaces if the book's name has spaces in it or leave them out. (e.g. 1 Kings and 1Kings both work)
* ```/bible``` can be replaced with ```/b```.
* ```[anonymous]``` may be replaced with an, anon, or anony.
* ```[chapter:verse]``` may be replaced with ```[chapter] [verse]```. (also ```<chapter:verse>``` with ```<chapter> <verse>```)
* Parameters may be typed in any order.

```
/bible [book] [chapter:verse] [translation]
/bible [alias] [book] [chapter] [verse] [translation]
/bible favorite:# [translation]
/bible favorite <#> [translation]
```
* Aliases: read, verseread, readverse, vread, and readv
* Shows you a Bible verse.
* Requires Permission: TadukooBible.verse.read
* Defaults:
	* ```[book]``` defaults to Genesis.
	* ```[chapter]``` defaults to 1.
	* ```[verse]``` defaults to 1.
	* ```[translation]``` defaults to whatever is set in the config.yml, which is KJV by default.
* ```[chapter]``` and ```[verse]``` can be replaced with #, info, or ?.
	* Replacing ```[chapter]``` will show book info.
	* Replacing ```[verse]``` will show the number of verses in the chapter you chose.

```
/bible send <player> <book> <chapter:verse> [translation] [anonymous] [bypass]
/bible send <player> favorite:# [translation] [anonymous] [bypass] 
/bible send <player> favorite <#> [translation] [anonymous] [bypass]
```
* Aliases: sendverse, versesend, giveverse, versegive, sendv, vsend, givev, and vgive.
* Sends a verse to another player.
* Requires permission: TadukooBible.verse.send
* ```[anonymous]``` makes it so you are anonymous in sending the verse.
	* Requires permission: TadukooBible.anonymous.verse
* ```[bypass]``` makes it so you can bypass verse sending settings.
	* Requires permission: TadukooBible.bypass.verse
* The player receiving the verse requires the TadukooBible.verse.receive permission.

```
/bible previous [type] [translation]
```
* Aliases: pre, prev, back, before, and b4.
* Shows you the Bible verse before the one you last read, by ```[type]```.
* ```[type]``` can be verse, v, chapter, chp, book, or b.
	* Verse type goes back one verse exactly.
	* Chapter type goes back to the beginning of the chapter. If already there, it goes back one chapter.
	* Book type goes back to the beginning of the book. If already there, it goes back one book.
* Gives a message if trying to go before Genesis 1:1.
* Requires permission: TadukooBible.verse.previous

```
/bible next [translation]
```
* Aliases: forward, for, after, aft, nextverse, versenext, nextv, and vnext.
* Shows you the Bible verse after the one you last read.
* Gives a message if trying to go after Revelation 22:21.
* Requires permission: TadukooBible.verse.next

```
/bible last [translation]
```
* Aliases: saved, save, load, lastverse, verselast, lastv, vlast, versesaved, savedverse, vsaved, savedv, vsave, versesave, loadverse, verseload, vload,
and loadv.
* Shows you the Bible verse you last read.
* Requires permission: TadukooBible.verse.last

```
/bible favorite [book] [chapter] [verse] [translation]
```
* Aliases: fav, favor, like, favoriteverse, versefavorite, favverse, versefav, favorverse, versefavor, likeverse, verselike, favoritev, vfavorite, favv, vfav,
favorv, vfavor, likev, and vlike.
* Allows you to favorite a Bible verse.
* ```[book]``` may be replaced with list and [chapter] with [page] to view a list of favorited verses.
* Requires Permission: TadukooBible.verse.favorite

```
/bible random [book] [chapter] [translation]
```
* Aliases: rand, randomverse, randomv, verserandom, vrandom, randverse, randv, verserand, and vrand.
* Shows a random verse.
* Requires permission: TadukooBible.verse.random

```
/bible getbook [book|"list"|random|previous:previousType|next:nextType|last] 
       [part] [translation] [?]
```
* Aliases: book, bookget, bibleget, getbible, bget, and getb.
* Gives you part of the Bible in book form.
* ```/bible getbook "list" [translation]``` gives you a book that lists all the books for that translation.
* ```/bible getbook previous``` will give you the previous book.
	* Defaults to going back by Minecraft book, not Bible book. (e.g. Exodus Book 1 to Genesis Book 17).
	* You can specify to go back by Minecraft book using ```"previous:part"```.
	* You can specify to go back by Bible book using ```"previous:book"```.
		* This will go back to Book 1 of the Bible book, unless Book 1 was the last book.
* ```/bible getbook next``` will give you the next book.
	* You can specify to go forward by Minecraft book using ```"next:part"```.
	* You can specify to go forward by Bible book using ```"next:book"```.
* ```/bible getbook last``` will give you the book you got last time you typed the command.
* ```/bible getbook random``` will give you a random book.
* Requires permission: TadukooBible.book.get
* Defaults:
	* ```[book]``` defaults to Genesis.
	* ```[part]``` defaults to 1.
	* ```[translation]``` defaults to whatever is set in the config.yml.
* Note: ```[part]``` is not the chapter.
* ? will tell you what is in that book.

```
/bible sendbook <player> <book> <part> [translation] [anonymous] [bypass]
```
* Aliases: booksend, sendbible, biblesend, givebook, bookgive, biblegive, givebible, sendb, bsend, giveb, and bgive.
* Sends part of a book of the Bible to a player.
* Requires permission: TadukooBible.book.send
* ```[translation]``` defaults to whatever is set in the config.yml.
* ```[anonymous]``` allows you to send the book anonymously.
	* Requires permission TadukooBible.anonymous.book
* ```[bypass]``` allows you to bypass book sending settings.
	* Requires permission: TadukooBible.bypass.book
* The player receiving the book requires the TadukooBible.book.receive permission.

```
/bible statistics [player|top] [statistic]
```
* Aliases: stats and stat.
* Allows you to view statistics of yourself.
* Currently cannot view other players' statistics (feature for 1.1 BETA 2)
* Currently cannot view top statistics or overall statistics (features for 1.1 BETA 2)
* Requires permission: TadukooBible.statistics.use to use.

```
/bible info [translation|book|permission|"plugin"|"books"|
             "translations"|"permissions"] [page]
```
* Aliases: about, abt, and information.
* Tells you information about the plugin, a translation, a book of the Bible, a permission, or lists books, translations, or permissions.
* Leaving no parameters defaults to showing plugin information.
* TadukooBible.info.plugin is required to view plugin information.
* TadukooBible.info.book is required to view book information.
* TadukooBible.info.translation is required to view translation information.
* TadukooBible.info.permission is required to view permission information.

```
/bible help [page|keyword]
```
* Aliases: ?, commands, commandshelp, cmds, and cmdshelp.
* Shows help for TadukooBible commands.
* Requires permission: TadukooBible.info.help

```
/bible plugin
```
* Aliases: TB, TadukooBible, TadukooBibleinfo, and plugininfo.
* Shows info about the plugin.
* Requires TadukooBible.info.plugin

```
/bible books [page|book]
```
* Aliases: bookslist, listbooks, booklist, booksinfo, bookinfo, infobooks, and infobook.
* Lists all the books in the Bible or shows info about a book.
* Requires permission: TadukooBible.info.book
* Books in red aren't available yet.
* Books in green are available.

```
/bible translation [translation]
```
* Aliases: translations, translist, translationslist, listtrans, tran, trans, translationinfo, translationsinfo, transinfo, and traninfo.
* Lists available translations or shows info about a translation.
* Requires permission: TadukooBible.info.translation

```
/bible permission [permission]
```
* Aliases: perm and perms.
* Lists the permissions or shows info about a permission.
* Requires permission: TadukooBible.info.permission

```
/bible config <setting> [value]
```
* Aliases: configuration, settings, set, and options.
* Shows or changes a setting in the config.yml.
* Requires permission: TadukooBible.op.config
* ```<setting>``` can be changed to list to list all the settings.

```
/bible announce <book> <chapter> <verse> [translation]
/bible announce <book> <chapter":"verse> [translation]
/bible announce favorite:# [translation]
/bible announce favorite <#> [translation]
```
* Aliases: ann, broadcast, broad, shout, and yell.
* Announce a Bible verse to the server.
* Requires the permission: TadukooBible.op.announce
* Requires TadukooBible.verse.announceget to see announcements.

```
/apocrypha
```
* Currently just gives messages about not being available yet.
* Added for future use.
* Requires permission: TadukooBible.apocrypha.use.

```
/apocrypha help
```
* Currently just gives you a message that no commands are available yet.
* Added for future use.
* Requires permission: TadukooBible.apocrypha.help.
