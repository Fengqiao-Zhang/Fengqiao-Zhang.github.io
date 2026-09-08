---
layout: default
title: "CV"
permalink: /cv/
---

<section class="section" markdown="1">

<details class="collapsible" open>
<summary>Awards</summary>
<ul class="timeline">
{% assign awards = site.data.awards %}
{% for item in awards %}
<li><span class="when">{{ item.date | replace: "-", "." }}</span><span>{{ item.text | markdownify | remove: "<p>" | remove: "</p>" }}</span></li>
{% endfor %}
</ul>
</details>


</section>

<section class="section" markdown="1">
<details class="collapsible" open>
<summary>Experience</summary>
- **2024.9–present** Assistant Professor, Delft University of Technology, the Netherlands.
- **2024.1-2024.8** MSCA Fellow, University of Cambridge, UK.
- **2022.10-2023.12** Postdoctoral researcher, Delft University of Technology, the Netherlands.
</details>
</section>

<section class="section" markdown="1">

<section class="section" markdown="1">
<details class="collapsible" open>
<summary>Education</summary>
- **2017.10–2022.9** PhD, Delft University of Technology, the Netherlands.
- **2015.9-2017.9** MSc, Delft University of Technology, the Netherlands.
- **2011.9-2015.6** BSc, Tongji University, China.
</details>
</section> 

