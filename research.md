---
layout: page
title: Research
permalink: /research/
---

<div class="pub-grid">
{% for p in site.data.papers %}
  <article class="pub-card">
    {% if p.image %}<a href="{{ p.url }}"><img src="{{ p.image | relative_url }}" alt="{{ p.title }}"></a>{% endif %}
    <div class="pub-body">
      <h3 class="pub-title"><a href="{{ p.url }}">{{ p.title }}</a></h3>
      <p class="pub-authors">{{ p.authors }}</p>
      <p class="pub-venue">{{ p.venue }}{% if p.year %} ({{ p.year }}){% endif %}</p>
      {% if p.blurb %}<p class="pub-blurb">{{ p.blurb }}</p>{% endif %}
      <p class="pub-links">
        <a href="{{ p.url }}">Link</a>
        {% if p.pdf %} · <a href="{{ p.pdf }}">PDF</a>{% endif %}
      </p>
    </div>
  </article>
{% endfor %}
</div>
