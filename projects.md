---
title: Projects
---
# Projects

{% for project in site.projects %}
## [{{project.title}}]({{project.url}})
{% if project.logo %}![{{project.title}}](/assets/images/{{project.logo}}){: style="float: left"}{% endif %}
{{project.summary}}
{% endfor %}
