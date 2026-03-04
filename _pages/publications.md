---
layout: archive
title: "Publications and Projects"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% assign selected_projects = site.portfolio | where_exp: "item", "item.title == 'PACCAR Summer 2024 Internship' or item.title == 'Hexapod Robot for Multi-Terrain Exploration (Work in Progress)' or item.title == 'Bionic Arm (Work in Progress)'" %}
{% assign publications = site.publications | concat: selected_projects | sort: "date" | reverse %}
{% for post in publications %}
  {% include archive-single-row.html %}
{% endfor %}
