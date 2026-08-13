---
layout: page
title: Labs
permalink: /labs/
---

Lab exercises by week (lecture slides are on the [Lectures](/lectures/) tab). Released
materials are visible to enrolled students.

{% comment %}
Labs are their own entries in the _lectures collection (`type: lab`). Sites synced
before that split carry their labs as "lab - ..." links on the lecture entry, so fall
back to the whole collection when there is no lab entry - the link filter below picks
the lab links out either way.
{% endcomment %}
{% assign lab_entries = site.lectures | where: "type", "lab" %}
{% if lab_entries.size == 0 %}{% assign lab_entries = site.lectures %}{% endif %}
{% assign lectures_sorted = lab_entries | sort: 'date' %}
{% for lecture in lectures_sorted %}
{% capture labs %}{% for link in lecture.links %}{% if link.name contains "lab -" %}<li><a href="{% if link.url contains '://' %}{{ link.url }}{% else %}{{ link.url | prepend: site.baseurl }}{% endif %}">{{ link.name | remove: "lab - " }}</a></li>{% endif %}{% endfor %}{% endcapture %}
{% if labs != "" %}
<h3>{{ lecture.title }}</h3>
<ul>{{ labs }}</ul>
{% endif %}
{% endfor %}
