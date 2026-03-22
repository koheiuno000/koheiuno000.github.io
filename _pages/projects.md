---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

{% include base_path %}

## Research-based Projects

{% assign research_projects = site.projects | where: "project_type", "Research-based" | sort: "date" | reverse %}
{% for post in research_projects %}
### [{{ post.title }}]({{ base_path }}{{ post.url }})
**Year:** {{ post.date | date: "%Y" }}

{{ post.excerpt }}
{% endfor %}

## Practice-based Projects

{% assign practice_projects = site.projects | where: "project_type", "Practice-based" | sort: "date" | reverse %}
{% for post in practice_projects %}
### [{{ post.title }}]({{ base_path }}{{ post.url }})
**Year:** {{ post.date | date: "%Y" }}

{{ post.excerpt }}
{% endfor %}