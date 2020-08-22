---
title: Tadukoo Bible Permissions Guide
blurb: How to use the permissions for the Tadukoo Bible plugin.
project: TadukooBible
---
This guide explains the permissions for [Tadukoo Bible](/projects/TadukooBible.html).

## Permissions
TadukooBible.*:
* Gives all permissions.
* Children:
	* TadukooBible.bible.*
	* TadukooBible.apocrypha.*
	* TadukooBible.debug

TadukooBible.bible.*:
* Gives all bible permissions.
* Children:
	* TadukooBible.use
	* TadukooBible.translation.*
	* TadukooBible.verse.*
	* TadukooBible.book.*
	* TadukooBible.info.*
	* TadukooBible.statistics.*
	* TadukooBible.block.*
	* TadukooBible.receive
	* TadukooBible.op.*
	* TadukooBible.anonymous.*
	* TadukooBible.bypass.*

TadukooBible.verse.*:
* Gives all verse permissions.
* Children:
	* TadukooBible.verse.read
	* TadukooBible.verse.send
	* TadukooBible.verse.receive
	* TadukooBible.verse.previous
	* TadukooBible.verse.next
	* TadukooBible.verse.last
	* TadukooBible.verse.favorite
	* TadukooBible.verse.random
	* TadukooBible.verse.announceget

TadukooBible.book.*:
* Gives all book permissions.
* Children:
	* TadukooBible.book.get
	* TadukooBible.book.send
	* TadukooBible.book.receive

TadukooBible.info.*:
* Gives all info permissions.
* Children:
	* TadukooBible.info.help
	* TadukooBible.info.plugin
	* TadukooBible.info.book
	* TadukooBible.info.translation
	* TadukooBible.info.permission

TadukooBible.statistics.*:
* Gives all statistics permissions.
* Children:
	* TadukooBible.statistics.use
	* TadukooBible.statistics.others
	* TadukooBible.statistics.top

TadukooBible.block.*:
* Gives all block permissions (view, verse, book, and immune).
* Children:
	* TadukooBible.block.view
	* TadukooBible.block.verse
	* TadukooBible.block.book
	* TadukooBible.block.immune

TadukooBible.op.*:
* Gives all op permissions.
* Children:
	* TadukooBible.op.config
	* TadukooBible.op.announce

TadukooBible.anonymous.*:
* Gives all anonymous permissions (verse and book).
* Children:
	* TadukooBible.anonymous.verse
	* TadukooBible.anonymous.book

TadukooBible.bypass.*:
* Gives all bypass permissions (verse and book).
* Children:
	* TadukooBible.bypass.verse
	* TadukooBible.bypass.book

TadukooBible.apocrypha.*:
* Gives all apocrypha permissions.
* Children:
	* TadukooBible.apocrypha.use
	* TadukooBible.apocrypha.info.help

TadukooBible.use:
* Required for use of plugin.
* Default: true

TadukooBible.translation.*:
* Gives all translation permissions (default, KJV, and OEB)
* Children:
	* TadukooBible.translation.default
	* TadukooBible.translation.KJV
	* TadukooBible.translation.OEB

TadukooBible.translation.default:
* Allows you to use the default translation. Overrides the translation's permission.
* Default: true

TadukooBible.translation.KJV:
* Allows you to use the KJV.
* Default: true

TadukooBible.translation.OEB:
* Allows you to use the OEB.
* Default: true

TadukooBible.verse.read:
* Allows use of /bible.
* Default: true

TadukooBible.verse.send:
* Allows use of /bible send.
* Default: op

TadukooBible.verse.receive:
* Allows you to receive verses.
* Default: true

TadukooBible.verse.previous:
* Allows use of /bible previous.
* Default: true

TadukooBible.verse.next:
* Allows use of /bible next.
* Default: true

TadukooBible.verse.last:
* Allows use of /bible last.
* Default: true

TadukooBible.verse.favorite:
* Allows use of /bible favorite.
* Default: true

TadukooBible.verse.random:
* Allows use of /bible random.
* Default: true

TadukooBible.announceget:
* Allows seeing announcements.
* Default: true

TadukooBible.book.get:
* Allows use of /bible getbook.
* Default: true

TadukooBible.book.send:
* Allows use of /bible givebook.
* Default: op

TadukooBible.book.receive:
* Allows you to receive books.
* Default: true

TadukooBible.info.help:
* Allows use of /bible help.
* Default: true

TadukooBible.info.plugin:
* Allows use of /bible plugin and using /bible info for plugin info.
* Default: true

TadukooBible.info.book:
* Allows use of /bible books and using /bible info for book info.
* Default: true

TadukooBible.info.translation:
* Allows use of /bible translation and using /bible info for translation info.
* Default: true

TadukooBible.info.permission:
* Allows use of /bible info for permission information.
* Default: op

TadukooBible.statistics.use:
* Allows use of /bible statistics (for your own statistics).
* Default: true

TadukooBible.statistics.others:
* Allows use of /bible statistics <nowiki><player> [statistic]</nowiki> to view other players' statistics.
* Default: op

TadukooBible.statistics.top:
* Allows use of /bible statistics top <nowiki><statistics></nowiki> to view top statistics.
* Default: op

TadukooBible.block.view:
* Allows using /bible block to view current information.
* Default: true

TadukooBible.block.verse:
* Allows using /bible block verse.
* Default: true

TadukooBible.block.book:
* Allows using /bible block book.
* Default: true

TadukooBible.block.immune:
* Makes you immune to being blocked with /bible block.
* Default: op

TadukooBible.receive:
* Allows use of /bible receive.
* Default: true

TadukooBible.op.config:
* Allows use of /bible config.
* Default: op

TadukooBible.op.announce:
* Allows use of /bible announce.
* Default: op

TadukooBible.anonymous.verse:
* Allows you to send verses anonymously.
* Default: op

TadukooBible.anonymous.book:
* Allows you to send books anonymously.
* Default: op

TadukooBible.bypass.verse:
* Allows you to bypass players.yml verse settings.
* Default: op

TadukooBible.bypass.book:
* Allows you to bypass players.yml book settings.
* Default: op

TadukooBible.apocrypha.use:
* Allows use of /apocrypha.
* Default: true

TadukooBible.apocrypha.info.help:
* Allows use of /apocrypha help.
* Default: true

TadukooBible.debug:
* Shows you debug messages.
* Default: false
