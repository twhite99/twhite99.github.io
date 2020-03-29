---
layout: archive
permalink: /projects/
title: "Data Science Projects by tags"
author_profile: TRUE
Header:
   image: "/images/Court_of_Sciences2.jpg"
---
{% include base_path %}
{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
