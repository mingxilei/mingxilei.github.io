<h2 id="publications" style="margin: 2px 0px -15px;">Publications</h2>

<div class="publications">
<p><small>(* indicates equal contribution.)</small></p>
<ol class="bibliography">

{% for link in site.data.publications.main %}

<li style="min-height: 0;">
<div class="pub-row">
  <div class="col-sm-9" style="position: relative; width: 100%; padding: 0;">
      <div class="title">
        {% if link.conference_short %}<span class="badge" style="background-color: var(--global-theme-color); margin-right: 0.5em;">{{ link.conference_short }}</span>{% endif %}
        {% if link.pdf %}<a href="{{ link.pdf }}">{{ link.title }}</a>{% else %}{{ link.title }}{% endif %}
      </div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em>
      </div>
    <div class="links">
      {% for resource in link.links %}
      <a href="{{ resource.url }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">{{ resource.label }}</a>
      {% endfor %}
      {% if link.notes %} 
      <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
      {% endif %}
      {% if link.others %} 
      {{ link.others }}
      {% endif %}
    </div>
  </div>
</div>
</li>
<br>

{% endfor %}

</ol>
</div>
