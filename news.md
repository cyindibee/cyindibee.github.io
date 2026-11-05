---
title: News
permalink: /news/
---

# News

{% assign news = site.news | sort: "date" | reverse %}
<ul class="news">
{% for n in news %}
  {% include news-item.html n=n %}
{% endfor %}
</ul>
