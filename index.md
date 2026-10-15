---
title: Home
---

<section class="hero">
  <h1>CyIndiBee</h1>
  <p class="lead">Computer vision and edge computing for monitoring individual honey bees — University of Puerto Rico, Río Piedras.</p>
  <p>
    <a class="btn primary" href="{{ site.wordpress_url }}">Visit the main site</a>
    <a class="btn" href="{{ '/publications/' | relative_url }}">Publications</a>
  </p>
</section>

## On the main site

<div class="cards">
  <a class="card" href="{{ site.wordpress_url }}">
    <strong>News &amp; posts</strong>
    <span>Latest updates, photos and project news.</span>
  </a>
  <a class="card" href="{{ site.wordpress_url }}">
    <strong>About the project</strong>
    <span>Goals, funding and collaborators.</span>
  </a>
  <a class="card" href="{{ '/team/' | relative_url }}">
    <strong>Team</strong>
    <span>Faculty and students working on CyIndiBee.</span>
  </a>
</div>

## Recent publications

<ul class="pubs">
{% assign pubs = site.publications | sort: "date" | reverse %}
{% for p in pubs limit: 3 %}
  {% include pub-item.html p=p %}
{% endfor %}
</ul>

<p><a href="{{ '/publications/' | relative_url }}">All publications →</a></p>
