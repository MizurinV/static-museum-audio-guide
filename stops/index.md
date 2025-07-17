---
layout: master
permalink: /stops/
---

<p>{{ site.index_page_text }}</p>

<ul class="post-list">
  {% assign stops = site.pages | where: "type", "stop" | sort: "page_rank" %}
  {% for stop in stops %}
    <li>
      <a class="post-link" href="{{ stop.url }}" 
         style="background-image: url('{{ site.baseurl }}{{ site.headphones_icon_color }}');">
        <span class="post-item">{{ stop.stop_id }}</span>
      </a>
    </li>
  {% endfor %}
</ul>