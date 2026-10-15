---
title: Team
permalink: /team/
# To add a person: copy a block below, fill it in, and put their photo in
# assets/img/team/ (square image, ~400x400). Leave `photo` out to show initials.
members:
  - name: Rémi Mégret
    role: Principal Investigator
    photo:
    link:
  - name: Team member
    role: Graduate student
    photo:
    link:
  - name: Team member
    role: Undergraduate student
    photo:
    link:
---

# Team

<div class="team">
{% for m in page.members %}
  <div class="member">
    {% if m.photo %}
      <img src="{{ m.photo | relative_url }}" alt="{{ m.name }}">
    {% else %}
      {% assign parts = m.name | split: " " %}
      <div class="avatar">{{ parts.first | slice: 0 }}{{ parts.last | slice: 0 }}</div>
    {% endif %}
    <div class="name">{% if m.link %}<a href="{{ m.link }}">{{ m.name }}</a>{% else %}{{ m.name }}{% endif %}</div>
    <div class="role">{{ m.role }}</div>
  </div>
{% endfor %}
</div>
