---
short_name: TadukooBible
title: Tadukoo Bible
logo: TadukooBiblePlugin.png
blurb: Tadukoo Bible is a plugin for Bukkit that allows you to read the Bible through commands or give yourself the book(s).
summary: >
  Tadukoo Bible is a plugin for Bukkit that allows you to read the Bible through commands or get it in Minecraft books. One Minecraft book contains several chapters of 
  a book of the Bible, but Bible books are not mixed within Minecraft books (A new Bible book starts a new Minecraft book).
---


**Note: After version 1.1, Tadukoo Bible's main server software will change. It may still be updated on Bukkit 1.7.9-R0.2, but will not be the main focus. 
What the main server software will become is unknown at this point.**

Current version: 1.1 Beta 1 [Bukkit 1.7.9-R0.2]

Upcoming version: 2.0 (Tentative Deadline: November 28, 2019)

## Features
* Read the Bible through commands (/bible).
* Send verses to other players (/bible send).
* Easily navigate forward or back in the Bible (/bible previous and /bible next and can be used in other commands as well).
* Show the last verse you read (/bible last and can be used in other commands as well).
* Save Bible verses in a favorites list (/bible favorite).
* Read a random Bible verse (/bible random).
* Get the Bible as books (/bible getbook).
* Send the Bible as books to other players (/bible sendbook).
* Get statistics of yourself, the whole server, others, or how you compare to others (/bible statistics).
* Get help with the plugin (/bible help).
* Get information about the books of the Bible (/bible books or /bible info).
* Get information about the various available translations of the Bible (/bible translation or /bible info).
* Get information about the plugin and its permissions (/bible plugin and /bible permission along with /bible info).
* Get a list of the books of the Bible (/bible books or /bible info).
* Get a list of the various available translations (/bible translation or /bible info).
* Change the config while in game (/bible config).
* Announce a Bible verse to the server (/bible announce).
* Automatically announce verses to the server (config.yml auto-announce settings).

**Make sure to read the installation as it contains some important information.**

## Usage
See the following pages for help with commands, permissions, and configuration.

[Tadukoo Bible Plugin Commands](/guides/tadukoo-bible-commands.html)

[Tadukoo Bible Plugin Permissions](/guides/tadukoo-bible-permissions.html)

[Tadukoo Bible Plugin Configuration](/guides/tadukoo-bible-configuration.html)

## Upcoming Commands/Features
[See this page for upcoming features and commands.](/TadukooBible/tadukoo-bible-upcoming-features.html)

If you have a feature,command, or alias to suggest, please use either BukkitDev's Ticket System or GitHub's Issue Tracker and label it as an Enhancement.

## Known Issues
None at the moment.

If you find an error, please report it using either BukkitDev's Ticket System (label it as Defect) or GitHub's Issue Tracker (label it as Bug).

## Translations
Currently the only translation in the plugin is the King James Version (KJV), which is public domain. In the future, I will be requesting permission
for other translations, unless they are in public domain in which case I can use them without permission as well.

Feel free to suggest what the next translation I add should be.

## Installation
Unzip the TadukooBible.zip file.

Place the TadukooBible.jar file and the Tadukoo_Bible folder into your plugins folder.

**Note: The Tadukoo_Bible folder contains the Bible verses! The plugin does not generate these files as it would cause the first load time to take 
hours (literally)!**

Run your server and you should be good to go.

## Translation Progress
Note: Translations that are not 100%, but say "max" are completed up to the amount they have. For example, the Open English Bible does not have all of the 
books of the Bible in it yet, so it will not say 100%.

King James Version (KJV) (100%)

Open English Bible (OEB) (0%)

[Want to see how the percentages are calculated?](/TadukooBible/tadukoo-bible-translation-progress.html)

## Version System
[See this page for how the version numbers are determined.](/TadukooBible/tadukoo-bible-version-system.html)

## The Story Behind the Plugin
The story contains information about why the 1.1 update is so far away from the 1.0 update, among other things.

[See this page for the story behind Tadukoo Bible.]({% post_url 2020-08-22-story-behind-tadukoo-bible %})

## Important Links
[GitHub plugin page](https://github.com/Tadukoo/TadukooBibleProject)

## Changelog
{% assign changelog = site.changelogs | where:"project", page.short_name | sort:"index" | last %}
[Click here to see the changelog for Tadukoo Bible.]({{changelog.url}})

## Other Notes
Thanks to Pew446 for helping me with getting the Minecraft books set up, and for his other suggestions on the plugin.

Thanks to ABDTGaming for his suggestions on the plugin as well.

Thanks to gamelover85 for helping with some of the book descriptions, and for his suggestions on the plugin.
