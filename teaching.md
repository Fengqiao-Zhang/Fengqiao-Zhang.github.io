---
layout: default
title: "Teaching"
permalink: /teaching/
---

<section class="section" markdown="1">
  <details class="collapsible" open>
    <summary>Teaching Activities</summary>
    <ul class="timeline">
      {% assign teaching = site.data.teaching %}
      {% for item in teaching %}
      <li><span class="when">{{ item.role }}</span><span>{{ item.type }} {{ item.title | markdownify | remove: "<p>" | remove: "</p>" }}, {{ item.venue }}.</span></li>
      {% endfor %}
    </ul>
  </details>
</section>
