---
title: Sitemap
---
# Sitemap

#### Table of Contents
* [Projects](#projects)
* [Stories](#stories)

## [About](/about.html)

## Projects
{% for project in site.projects %}- [{{project.title}}]({{project.url}}) - {{project.blurb}}
{% assign projectPages = site.pages | where:"category", project.short_name %}{% for projectPage in projectPages %}
	* [{{projectPage.title}}]({{projectPage.url}}){% endfor %}
{% endfor %}

## Stories
{% for story in site.stories %}- [{{story.title}}]({{story.url}}) - {{story.blurb}}
{% endfor %}
