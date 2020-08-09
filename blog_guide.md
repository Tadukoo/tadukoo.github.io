---
title: Blog Guide
---
# Blog Guide

#### Table of Contents
* [Programming](#programming)
	* [General](#general)
	* [Games](#games)
		* [T.A.D.U.K.O.O. I.S. T.H.E. G.R.E.A.T.E.S.T. P.E.R.S.O.N. W.H.O. E.V.E.R. L.I.V.E.D.](#tadukoo-is-the-greatest-person-who-ever-lived)
* [Beliefs](#beliefs)
	* [General](#general-1)
	* [Tadukoo Bible Project](#tadukoo-bible-project)
* [Videos](#videos)
* [Plans](#plans)
* [And More](#and-more)
* [Blog Updates](#blog-updates)
	* [Blogger Updates](#blogger-updates)

## Programming
Posts about my programming.

### General
General posts about programming that don't fall under any subcategories

{% assign genProgPosts = site.posts | where:"series", "General Programming" | sort:"index" %}
{% for genProgPost in genProgPosts %}{{genProgPost.index}}. [{{genProgPost.title}}]({{genProgPost.url}}) - {{genProgPost.date | date_to_string}}
{% endfor %}

### Games
Posts about games I've programmed.

### T.A.D.U.K.O.O. I.S. T.H.E. G.R.E.A.T.E.S.T. P.E.R.S.O.N. W.H.O. E.V.E.R. L.I.V.E.D.
A specific joke game I was working on in the past.

{% assign tagPosts = site.posts | where:"series", "TAG" | sort:"index" %}
{% for tagPost in tagPosts %}{{tagPost.index}}. [{{tagPost.title}}]({{tagPost.url}}) - {{tagPost.date | date_to_string}}
{% endfor %}

## Beliefs
Posts that focus more on my beliefs, mainly as a Christian.

### General
General posts about my beliefs that don't fall under any subcategories

{% assign genBelPosts = site.posts | where:"series", "General Beliefs" | sort:"index" %}
{% for genBelPost in genBelPosts %}{{genBelPost.index}}. [{{genBelPost.title}}]({{genBelPost.url}}) - {{genBelPost.date | date_to_string}}
{% endfor %}

### Tadukoo Bible Project
Tadukoo Bible Project is an expression I've used for various things, but on this blog it's been used to talk about my beliefs with it.

{% assign tbpPosts = site.posts | where:"series", "TBP" | sort:"index" %}
{% for tbpPost in tbpPosts %}{{tbpPost.index}}. [{{tbpPost.title}}]({{tbpPost.url}}) - {{tbpPost.date | date_to_string}}
{% endfor %}

## Videos
I've made YouTube videos in the past, and would like to in the future

{% assign vidPosts = site.posts | where:"series", "Videos" | sort:"index" %}
{% for vidPost in vidPosts %}{{vidPost.index}}. [{{vidPost.title}}]({{vidPost.url}}) - {{vidPost.date | date_to_string}}
{% endfor %}

## Plans
Every so often, I make a big post about general plans of stuff I want to do

{% assign planPosts = site.posts | where:"series", "Plans" | sort:"index" %}
{% for planPost in planPosts %}{{planPost.index}}. [{{planPost.title}}]({{planPost.url}}) - {{planPost.date | date_to_string}}
{% endfor %}

## And More
Some posts just don't fall under a category

{% assign morePosts = site.posts | where:"series", "And More" | sort:"index" %}
{% for morePost in morePosts %}{{morePost.index}}. [{{morePost.title}}]({{morePost.url}}) - {{morePost.date | date_to_string}}
{% endfor %}

## Blog Updates
Updates about the blog in general.

{% assign blogUpdates = site.posts | where:"series", "Blog Updates" | sort:"index" %}
{% for blogUpdate in blogUpdates %}{{blogUpdate.index}}. [{{blogUpdate.title}}]({{blogUpdate.url}}) - {{blogUpdate.date | date_to_string}}
{% endfor %}

### Blogger Updates
Updates that were copied over from the old Blogger site (and aren't 100% relevant here anymore)

{% assign bloggerUpdates = site.posts | where:"series", "Blogger Updates" | sort:"index" %}
{% for bloggerUpdate in bloggerUpdates %}{{bloggerUpdate.index}}. [{{bloggerUpdate.title}}]({{bloggerUpdate.url}}) - {{bloggerUpdate.date | date_to_string}}
{% endfor %}
