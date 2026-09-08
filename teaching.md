---
layout: default
title: "Teaching"
permalink: /teaching/
---

<section class="section" markdown="1">

{% for course in site.teaching %}
## {{ course.title }}
*{{ course.type }}, {{ course.venue }}, {{ course.location }} — {{ course.date | date: "%B %Y" }}*

{{ course.content | markdownify }}
{% endfor %}

</section>
