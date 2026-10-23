---
title: Team
permalink: /team/
# People are edited in _data/team.yml, not here.
groups:
  - id: faculty
    title: Faculty
  - id: researcher
    title: Researchers
  - id: graduate
    title: Graduate students
  - id: undergraduate
    title: Undergraduate students
  - id: alumni
    title: Alumni
---

# Team

{% for g in page.groups %}
{% assign people = site.data.team | where: "group", g.id %}
{% if people.size > 0 %}
<h2>{{ g.title }}</h2>
<div class="team">
{% for m in people %}
  <article class="member">
    <div class="member-head">
      {% if m.photo %}
        <img src="{{ m.photo | relative_url }}" alt="{{ m.name }}">
      {% else %}
        {% assign parts = m.name | split: " " %}
        <div class="avatar">{{ parts.first | slice: 0 }}{{ parts.last | slice: 0 }}</div>
      {% endif %}
      <div>
        <div class="name">{{ m.name }}</div>
        {% if m.program %}<div class="role">{{ m.program }}</div>{% endif %}
      </div>
    </div>
    {% if m.project %}<p class="project">{{ m.project }}</p>{% endif %}
    {% if m.bio %}<p class="bio">{{ m.bio }}</p>{% endif %}
    {% if m.advisor %}<p class="meta">Advisor: {{ m.advisor }}</p>{% endif %}
    {% if m.links and m.links.size > 0 %}
    <p class="meta">{% for l in m.links %}<a href="{{ l.url }}">{{ l.label }}</a>{% unless forloop.last %} · {% endunless %}{% endfor %}</p>
    {% endif %}
  </article>
{% endfor %}
</div>
{% endif %}
{% endfor %}
