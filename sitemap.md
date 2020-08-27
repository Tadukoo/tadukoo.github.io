---
title: Sitemap
---
# Sitemap

#### Table of Contents
* [Blog](#blog)
* [Projects](#projects)
* [Stories](#stories)

## [About](/about.html)

## Blog
There are many blog posts compared to the other types of pages.
- For the most recent posts, [go here](/blog.html)
- For an index by series/topic, [go here](/blog_guide.html)

## Projects
{% for project in site.projects %}- [{{project.title}}]({{project.url}}) - {{project.blurb}}
{% assign projectPages = site.pages | where:"category", project.short_name %}{% for projectPage in projectPages %}
	* [{{projectPage.title}}]({{projectPage.url}}){% endfor %}
{% endfor %}

## Stories
{% for story in site.stories %}- [{{story.title}}]({{story.url}}) - {{story.blurb}}
{% endfor %}
