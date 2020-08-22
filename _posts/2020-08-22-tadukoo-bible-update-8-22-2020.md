---
title:  "Tadukoo Bible Update 8/22/2020"
author: Tadukoo
date:   2020-08-22 15:25
series: "Tadukoo Bible"
index: 1
categories: blog
tags: 
- Programming
- Tadukoo Bible
comment_issue_id: 33
---
I've moved the information for Tadukoo Bible to this website finally (it used to be on [my wiki](https://tadukooverse.wikia.com) - which includes a bunch of stuff I've done, and 
some more of that will likely move over here in the future, but not all of it). From now on, this site will be the main place for Tadukoo Bible information (specifically from its 
[project page](/projects/TadukooBible.html)).

Tadukoo Bible has been on a bit of a hiatus for a long time now, mainly due to college and other projects taking priority over the past several years for me. Last I touched it, 
I was trying to convert it into a general thing instead of just a Bukkit plugin, and trying to make a generic Minecraft API, and changing it to download verses from BibleHub 
to use instead of me having to setup the verse files by copy-paste (like I did for the King James Version back in the day). The general conversion and Minecraft API didn't get 
very far, but I do have working code to download from BibleHub (it's just not in the plugin itself).

I still want to do all of those plans, and add a bunch of the features in the [upcoming features list](/TadukooBible/tadukoo-bible-upcoming-features.html), but I also want to 
place a priority on my work with the Tadukooverse stuff (Tadukoo Util and Tadukoo Engine/Launcher - 
see [the Tadukooverse master plan](https://tadukooverse.github.io/2020/08/14/the-tadukooverse-master-plan.html)). At some point in the near future, I'd like to sit down and 
come up with a proper plan for Tadukoo Bible moving forward to get everything done for it (Tadukoo Bible Master Plan?).

Most of the conversion and Minecraft API stuff is due to Bukkit essentially dying (I like to say it's on life support right now). I know you can still get Bukkit at the moment 
through Spigot (but that they recommend using Spigot instead of Bukkit anyway, and they're close to being the same thing now). But back when Bukkit got its DMCA takedown, 
I wasn't sure what would happen moving forward with it and started my own plans to move on (at least mentally, you can tell on GitHub I didn't get far with it). My plan 
was to release Tadukoo Bible 1.1 for Bukkit 1.7.9 (the last version before the DMCA) and then figure out a new server software to switch to (which probably would've been 
Sponge). At some point that plan evolved to make my own Minecraft API that can connect to other APIs (Bukkit, Spigot, Sponge, etc.) so that you write a plugin once and 
can use it on any server software (in theory). Your plugin would use my API's methods, and my API would be implemented by a connector plugin in Bukkit or whichever 
server software (and if you want a standalone, you can include my connector plugin logic in your plugin). So that's where the Minecraft API idea came from and what it 
is supposed to be eventually.

The converting to a general thing relates to that too. Why stop at enabling it for general Minecraft server software? Why not also make it so you can have a standalone 
program that can show you the Bible verses and do the conversions to Minecraft as needed (e.g. downloading translations to the verse files)? With this, the plan became 
making a Tadukoo Bible API that would be implemented in both a Minecraft form (via the Minecraft API I would make) and in a standalone command (or GUI?) program.

As for the additional features, someone had suggested a long time ago that I just download the verses automatically from Bible Gateway. Tadukoo Bible was the first 
major programming project I did, so if you look at the earliest code for it, it's all a mess. I had originally hard-coded the verses in the classes, it was terrible. 
So leading up to v.1.0, I probably didn't know how to download them from anywhere. I tend to use BibleHub instead of Bible Gateway, that's why I chose it instead. 
But using any website to download the verses greatly opens up the number of translations that can be used. Of all the ideas for future features, this one is 
the most significant in my opinion, and I haven't even explained all the changes it requires.

Firstly, it requires checking if you already downloaded the verses or not, and being able to download the verses in general. Then I'd add a command to download an 
entire translation (mainly for admins to use when the server isn't being actively used so it's ready for later). So far not so hard, but there's a problem. To get 
it as Minecraft books, I've been using a separate plugin (Tadukoo Bible Books) to parse the verses into a nice format for use in Minecraft books. So that plugin 
needs to be combined into Tadukoo Bible and get changed to run when people try to get books (and trigger the verse download if needed). Also, since the book 
conversion would now be happening on the server, it needs to be optimized (which I ended up writing a parallel version as a college project, but it's not connected 
to the other stuff yet, it's a separate program that just does that conversion).

There are a few other ideas related to the Tadukoo Bible Books stuff. I wanted to make it so you can make your own books (e.g. compile your favorite verses) and 
verses on certain topics, commentaries, the apocrypha, testimonies (there were a bunch of alternate book ideas). So this would be more changes to the books stuff 
(it's currently setup specifically for setting up Minecraft books with books of the Bible). Ultimately, I was thinking of changing Tadukoo Bible Books into another 
Minecraft based API to extend my base Minecraft API, perhaps a "Minecraft Books API". It would allow for generic conversion of books by their chapter and verse/sentence 
references to be able to be put in Minecraft books (i.e. go beyond just the Tadukoo Bible book ideas, and allow for anyone to take any book and put it through this).

The other things on the upcoming features probably wouldn't cause as significant changes as those listed above, but there's still a handful of work to do for those 
features as well.
