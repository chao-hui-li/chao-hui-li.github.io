<h2 id="talks">Talks</h2>

<ul class="talk-list" aria-label="Research talks, most recent first">
  {% for talk in site.data.talks.main %}
  <li class="talk-item">
    <article aria-labelledby="talk-title-{{ forloop.index }}">
      <h3 class="talk-title" id="talk-title-{{ forloop.index }}">{{ talk.title | escape }}</h3>
      <p class="talk-meta"><a href="{{ talk.event_url | escape }}" target="_blank" rel="noopener" aria-label="Event information for {{ talk.event | escape }}, {{ talk.date_label | escape }}">{{ talk.event | escape }}</a>&ensp;<span>{{ talk.location | escape }}</span>&ensp;<time datetime="{{ talk.date }}">{{ talk.date_label | escape }}</time></p>
      {% if talk.highlight %}
      <p class="talk-highlight">{{ talk.highlight | escape }}</p>
      {% endif %}
    </article>
  </li>
  {% endfor %}
</ul>
