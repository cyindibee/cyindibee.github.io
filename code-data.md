---
title: Code & Data
permalink: /code-data/
# Add one block per repository or dataset.
resources:
  - title: CyIndiBee on GitHub
    kind: Code
    url: https://github.com/cyindibee
    description: Source code for the project, including this website.
---

# Code & Data

{% for r in page.resources %}
<article class="resource">
  <p class="resource-kind">{{ r.kind }}</p>
  <h3><a href="{{ r.url }}">{{ r.title }}</a></h3>
  <p>{{ r.description }}</p>
</article>
{% endfor %}
