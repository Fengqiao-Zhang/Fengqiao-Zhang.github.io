---
layout: default
title: "Teaching"
permalink: /teaching/
---

<section class="section" markdown="1">
  <details class="collapsible" open>
    <summary>Courses</summary>
    <ul class="timeline">
      {% assign teaching = site.data.teaching %}
      {% for item in teaching %}
      <li><span class="when">{{ item.role }}</span><span>{{ item.type }} {{ item.title }}, {{ item.venue }}.</span></li>
      {% endfor %}
    </ul>
  </details>
</section>
