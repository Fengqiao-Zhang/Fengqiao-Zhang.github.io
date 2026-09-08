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
<ul class="timeline">
<li><span class="when">2024.9–present</span><span> Assistant Professor, Delft University of Technology, the Netherlands.</span></li>
<li><span class="when">2024.1–2024.8</span><span> MSCA Fellow, University of Cambridge, UK.</span></li>
<li><span class="when">2022.10–2023.12</span><span> Postdoctoral researcher, Delft University of Technology, the Netherlands.</span></li>
</ul>
</details>
</section>

<section class="section" markdown="1">
<details class="collapsible" open>
<summary>Education</summary>
<ul class="timeline">
<li><span class="when">2017.10–2022.9</span><span> PhD, Delft University of Technology, the Netherlands.</span></li>
<li><span class="when">2015.9–2017.9</span><span> MSc, Delft University of Technology, the Netherlands.</span></li>
<li><span class="when">2011.9–2015.6</span><span> BSc, Tongji University, China.</span></li>
</ul>
</details>
</section>
