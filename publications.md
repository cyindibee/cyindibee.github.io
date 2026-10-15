---
title: Publications
permalink: /publications/
---

# Publications

{% assign pubs = site.publications | sort: "date" | reverse %}
{% assign by_year = pubs | group_by: "year" %}

<nav class="year-menu">
  {% for y in by_year %}<a href="#y{{ y.name }}">{{ y.name }}</a>{% endfor %}
</nav>

{% for y in by_year %}
<h2 id="y{{ y.name }}">{{ y.name }}</h2>
<ul class="pubs">
  {% for p in y.items %}
    {% include pub-item.html p=p %}
  {% endfor %}
</ul>
{% endfor %}
