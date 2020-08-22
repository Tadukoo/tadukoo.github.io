---
title: Tadukoo Bible Alpha Changelog
project: TadukooBible
index: 1
---
You can see what changes were made to each file on [the GitHub commits page](https://github.com/Tadukoo/TadukooBibleProject/commits/master).

#### Table of Contents
* [Alpha 0.1.8 (July 17, 2014)](#alpha-018-july-17-2014)
* [Alpha 0.1.6.1 (May 20, 2014)](#alpha-0161-may-20-2014)
* [Alpha 0.1.6 (May 19, 2014)](#alpha-016-may-19-2014)
* [Alpha 0.1.4 (May 18, 2014)](#alpha-014-may-18-2014)
* [Alpha 0.1.2.6 (November 4, 2013)](#alpha-0126-november-4-2013)
* [Alpha 0.1.2.5 (October 31, 2013)](#alpha-0125-october-31-2013)
* [Alpha 0.1.2.4 (October 29, 2013)](#alpha-0124-october-29-2013)
* [Alpha 0.1.2.3 (October 28, 2013)](#alpha-0123-october-28-2013)
* [Alpha 0.1.2.2 (October 27, 2013)](#alpha-0122-october-27-2013)
* [Alpha 0.1.2.1 (October 26, 2013)](#alpha-0121-october-26-2013)
* [Alpha 0.1.2 (October 20, 2013)](#alpha-012-october-20-2013)
* [Alpha 0.1.0.3 (October 19,2013)](#alpha-0103-october-19-2013)
* [Alpha 0.1.0.2 (October 16, 2013)](#alpha-0102-october-16-2013)
* [Alpha 0.1.0.1 (October 15, 2013)](#alpha-0101-october-15-2013)
* [Alpha 0.1 (October 1, 2013)](#alpha-01-october-1-2013)
* [Alpha 0.0.9.33 (September 29, 2013)](#alpha-00933-september-29-2013)
* [Alpha 0.0.9 (September 28, 2013)](#alpha-009-september-28-2013)
* [Alpha 0.0.8.5 (August 13, 2013)](#alpha-0085-august-13-2013)
* [Alpha 0.0.8 (August 6, 2013)](#alpha-008-august-6-2013)
* [Alpha 0.0.6 (August 5, 2013)](#alpha-006-august-5-2013)
* [Alpha 0.0.4 (July 26, 2013)](#alpha-004-july-26-2013)
* [Alpha 0.0.2 (July 26, 2013)](#alpha-002-july-26-2013)
* [Alpha 0.0.1 (July 24, 2013)](#alpha-001-july-24-2013)
* [Alpha 0.0.0.60 (July 23, 2013)](#alpha-00060-july-23-2013)
* [Pre-Alpha 0.0.0.0 (July 20, 2013)](#pre-alpha-0000-july-20-2013)

## Alpha 0.1.8 (July 17, 2014)
* Added Luke.
* Changed a bit of the code in preparation for the future of the plugin.

## Alpha 0.1.6.1 (May 20, 2014)
* Some book config files were missing their "Lim" values.

## Alpha 0.1.6 (May 19, 2014)
* Added Mark

## Alpha 0.1.4 (May 18, 2014)
* Reorganized files and moved book checking to a separate plugin.
* Updated to Bukkit 1.7.9-R0.1.
* Added Matthew.
* Changed some names.

## Alpha 0.1.2.6 (November 4, 2013)
* Added ```/bible config```
* Added ```/bible announce```

## Alpha 0.1.2.5 (October 31, 2013)
* Added ```/bible random```
* Combined various classes into new ones.
* Started Matthew.yml

## Alpha 0.1.2.4 (October 29, 2013)
* Added ```/bible givebook```
* Added aliases for ```/bible getbook```
* Updated ```/bible help```
* You can now type ```/bible getbook <cmd>```, ```<cmd>``` being next, previous, or last, giving you the book after the last one you got, before, or the one you got last,
respectively.

## Alpha 0.1.2.3 (October 28, 2013)
* EnumCmds is now used for commands.
* Added TadukooBible.getbook permission.
* Added ```/bible help```
* Permissions are now checked using a separate method in MainCommandExecutor.
* There are now more permissions.
* Now a new book starts with an entire verse, rather than in the middle of one.
* Now you can type ```/bible getbook <book> <part #> ?``` to see what's in that book. It will display as ```"<book> Part <part #> contains #:#-#:#."```

## Alpha 0.1.2.2 (October 27, 2013)

### Command Changes
* Translation is now optional for most commands.
* Translation is now at the end of commands instead of the beginning.
* ```/bible list|?``` is now ```/bible translations|tranlist```
* ```/bible <translation> books|list``` is now ```/bible books|bookslist [page]```
* ```/bible book``` now has the alias ```/bible getbook```

### Permissions Changes
* ```/bible getbook|book [book] [part #] [translation]``` now requires TadukooBible.getbook
* Permissions can be enabled or disabled in the config.yml.
* Added permissions checking class.

### Other Changes
* Added early code for some future commands in EnumBooks.

## Alpha 0.1.2.1 (October 26, 2013)
* Default translation configurable in config.yml.

## Alpha 0.1.2 (October 20, 2013)
* An error in MainCommandExecutor was fixed.
* BooksList now shows Deuteronomy in green instead of red.
* Made changes in CheckTranslations to reduce size in the future (when more translations are available).
* Deuteronomy finished.
* Made it so in books the first verse in each chapter doesn't have a "1" before it.

## Alpha 0.1.0.3 (October 19, 2013)
* Now verses aren't cut off between pages.
* How often you get a notification of chapters being finished can be configured.
* Parts of verses don't go missing from books.
* NullPointerExceptions were fixed.
* Typos were fixed in the CheckBooks class.
* igBooks(in game books)'s configs are now named ```<translation>bookconfig.yml``` instead of ```<translation>config.yml```.
* Simplified MainCommandExecutor.

## Alpha 0.1.0.2 (October 16, 2013)
* Fixed books ending one page short.
* Fixed books being checked without numbers (if they have one)
* Fixed books being named what you type rather than the actual book's name.
* Fixed null pointer exceptions when leaving out bookName or Part # arguments in ```/bible <translation> book [bookName] [Part#]```.

## Alpha 0.1.0.1 (October 15, 2013)
* Now on a server start, books are determined and placed in a config file.
* In the future, there will be an option in the config.yml with this.
* Also, Deuteronomy was started.
* Books should now work.

## Alpha 0.1 (October 1, 2013)
* The Bible folder is now separate and should be placed in the plugins/Tadukoo Bible folder. If it is not there, the plugin will not work correctly. The books
list will continue to have different colors until all the books are completed in yml files. In game books will not be available for a while.
* Numbers is completed.
* KJV is now configurable in config.yml, and is only listed in available translations if set to true in the config.
* Now getting info or number of verses/chapters is re-enabled.

## Alpha 0.0.9.33 (September 29, 2013)
* Numbers has been completed up to chapter 24.
* The main class had methods added to it for future use for the books up through Beta 0.2.
* Now if a verse is null, it will send an error message to the user, rather than just saying "null".

## Alpha 0.0.9 (September 28, 2013)
* Changing the set-up of the plugin.
* Genesis, Exodus, Leviticus, Numbers 1 - 9, 1 John, 2 John, and 3 John changed to new set-up.
* KJVGenesis.java and KJVExodus.java have been moved.
* The package com.gmail.lucario77777777.TBP.commands.KJV.Genesis is gone because none of those files are needed with the new set-up of the
plugin.
* The package com.gmail.lucario77777777.TBP.commands.KJV.bible.Genesis will be gone eventually, but is still there so the verses can be copied
from those classes into Genesis.yml.
* A config.yml is added for future use to enable or disable translations.
* Numbers 10 - 17 added.

## Alpha 0.0.8.5 (August 13, 2013)
* Added Numbers 1 - 9.
* Made an enum for the books and their aliases.
* Fixed it saying Genesis isn't available for all non-existant books.
* Fixed errors with aliases not working.
* Tried changing the way the verses are set-up using delimiters, but failed. Because of this, Genesis Chapter 1 will give errors.

## Alpha 0.0.8 (August 6, 2013)
*Added Leviticus.

## Alpha 0.0.6 (August 5, 2013)
* Added Exodus.
* If a book isn't in the plugin yet, a message is now given saying we don't have it yet.

## Alpha 0.0.4 (July 26, 2013)
* Added 1, 2, and 3 John.
* Fixed an issue in Genesis.

## Alpha 0.0.2 (July 26, 2013)
* Finished Genesis.
* Made it so books shown using /bible kjv books are color coded (green = 100% complete, yellow = partially complete, red = 0% complete)

## Alpha 0.0.1 (July 24, 2013)
* Finished up to Genesis 25.

## Alpha 0.0.0.60 (July 23, 2013)
* Finished up to Genesis Chapter 15.
* Added to the first Genesis Book, but that introduced an issue: Pages 3 and 5 cut off part of the verse.

## Pre-Alpha 0.0.0.0 (July 20, 2013)
* Inital Commit.
