---
layout: default
title: "Service"
permalink: /service/
---

<section class="section" markdown="1">

<details class="collapsible" open>
<summary>Service</summary>
<ul class="timeline">
{% assign services = site.data.service | where: "type", "service" %}
{% for item in services %}
<li><span class="when">{{ item.date | replace: "-", "." }}</span><span>{{ item.text | markdownify | remove: "<p>" | remove: "</p>" }}</span></li>
{% endfor %}
</ul>
</details>

<details class="collapsible" open>
<summary>Activities</summary>
<ul class="timeline">
{% assign activities = site.data.service | where: "type", "activity" %}
{% for item in activities %}
<li><span class="when">{{ item.date | replace: "-", "." }}</span><span>{{ item.text | markdownify | remove: "<p>" | remove: "</p>" }}</span></li>
{% endfor %}
</ul>
</details>

</section>
