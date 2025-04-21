---
layout: page
title: Workshops
---

<ul>
{% for thing in site.pages %}
    {% if thing.type == "workshop" %}
    <li>
    <a href="{{ thing.url }}">{{ thing.title }}</a>
    </li>
    {% endif %}
    {% endfor %}
</ul>
