---
title: Tadukoo Bible Configuration Guide
blurb: How to config the Tadukoo Bible plugin.
project: TadukooBible
---
This guide explains how to configure [Tadukoo Bible](/projects/TadukooBible.html).

## Config.yml
```
version: '1.1 BETA 1'
# NEVER CHANGE THIS SETTING!

language: en_US
# This decides the language the plugin will use.
# You may type the name of the language or its abbreviation and it will change 
# to the default for that language.

startup-checks: true
# This checks for errors in this file on startup.

statistics:   
  plugin: true
  player:
    enabled: true
# These decide whether to keep track of statistics.
# player statistics is for statistics per player, while plugin statistics is 
# for everyone on the server.

default:
  translation: KJV 
  book: Genesis
  chapter: '1'
  verse: '1'
  part: '1'
# These are the book, chapter, verse, part, and translation used for commands 
# when none is specified.
# chapter, verse, and part must be a number in single quotes.

permissions: true
# This decides whether to use permissions or not.
# Note: If you use a permissions plugin and set TadukooBible.use to false, it 
# will still disable use of the plugin even if this is false.

books: true
# This will disable getting the Bible as books if set to false.
# Note: You could always just get the book config for your translation from 
# the site.

debug: false
# This will show messages to help find errors in the plugin if set to true.

# Translations Section
# Enable or disable translations here.
#(Note: You must still have the files for that translation or it won't work.)
KJV: true
OEB: true

# Auto-Announce Section
# This section is for auto-broadcasting verses to the server every so often.
# You can add or remove as many verses as you want.
# Random as a verse reference will broadcast a random verse.
# Random may be used in either a randomized-list, an ordered list, 
# or by itself.
auto-announce:
  enabled: false
  randomize-list: false
  # Makes it so that a random reference is chosen each time from the list, 
  # rather than going in order.
  delay: 1
  # Delay is in minutes.
  verses:
  - Genesis 1:1
  - John 3:16
  - random
  ```
