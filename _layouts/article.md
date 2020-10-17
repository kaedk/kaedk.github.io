---
layout: page
hide_hero: false
---

<div class="columns is-multiline mb-6">
  <div class="column is-8 is-offset-2">
    <p class="title is-3 is-size-1 has-text-centered is-family-monospace">
      {{ page.title }}
    </p>
    <p class="subtitle is-3 has-text-centered is-family-monospace">
      [{{ page.subtitle }}]
    </p>
    <p class="subtitle is-4 has-text-centered is-family-monospace mb-6">
      "{{ page.description }}"
    </p>

    <div class="content columns is-multiline">
        {{ content }}
        {% for part in page.parts %}
          <p class="column is-8 is-offset-2 has-text-centered">
            <span class="is-italic">({{ forloop.index }})</span><br>
            {{ part }}
          </p>
        {% endfor %}
    </div>
    <div class="content">
      {% if site.disqus.shortname %}
        {% include disqus.html %}
      {% endif %}
    </div>
  </div>
</div>
