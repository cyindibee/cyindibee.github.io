---
title: Home
---

<section class="hero{% if site.hero_image %} has-image{% endif %}">
  <div class="hero-text">
    <h1>CyIndiBee</h1>
    <p class="lead">CyberInfrastructure for video analysis of individual bee behavior. We build computer vision tools that track and identify individual honey bees in video, so biologists can study their behavior at scale.</p>
    <p class="hero-meta">University of Puerto Rico, Río Piedras</p>
  </div>
  {% if site.hero_image %}
  <img class="hero-image" src="{{ site.hero_image | relative_url }}" alt="{{ site.hero_image_alt }}">
  {% endif %}
</section>

## Learn more

<div class="cards learn-more">
  <a class="card" href="{{ '/about/' | relative_url }}">
    <strong>About the project</strong>
    <span>Goals, approach and funding.</span>
  </a>
  <a class="card" href="{{ '/team/' | relative_url }}">
    <strong>Team</strong>
    <span>Faculty, students and collaborators.</span>
  </a>
  <a class="card" href="{{ '/publications/' | relative_url }}">
    <strong>Publications</strong>
    <span>Papers produced by the project.</span>
  </a>
  <a class="card" href="{{ '/code-data/' | relative_url }}">
    <strong>Code &amp; Data</strong>
    <span>Software and datasets.</span>
  </a>
</div>

## Recent news

{% assign news = site.news | sort: "date" | reverse %}
<ul class="news">
{% for n in news limit: 3 %}
  {% include news-item.html n=n %}
{% endfor %}
</ul>

<p><a class="btn" href="{{ '/news/' | relative_url }}">More news</a></p>
