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

{% assign publications = site.publications | sort: "date" | reverse %}
{% for post in publications %}
  {% include archive-single-row.html %}
{% endfor %}

{% assign projects = site.portfolio | sort: "date" | reverse %}
{% for post in projects %}
  {% if post.title == "PACCAR Summer 2024 Internship" %}
    {% include archive-single-row.html %}
  {% endif %}
  {% if post.title == "Hexapod Robot for Multi-Terrain Exploration" %}
    {% include archive-single-row.html %}
  {% endif %}
  {% if post.title == "Bionic Arm" %}
    {% include archive-single-row.html %}
  {% endif %}
{% endfor %}
