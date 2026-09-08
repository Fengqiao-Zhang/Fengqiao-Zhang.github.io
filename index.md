---
layout: default
permalink: /
---

<section class="section" markdown="1">

<!-- # Hi, I'm Fengqiao Zhang. -->

I am an Assistant Professor at the Delft University of Technology, specializing in intelligent monitoring, structural assessment, and service-life prediction of concrete infrastructure. My research has been internationally recognized with the IABSE Best PhD Thesis Award and a prestigious Dutch Research Council (NWO) VENI grant. Before joining the faculty at TU Delft, I was a Marie Skłodowska-Curie Actions Fellow at the University of Cambridge, where I worked on integrating infrastructure monitoring with probabilistic modelling. I have also contributed to major research programmes with government and industry on the assessment of existing concrete bridges. Beyond research, I play an active international leadership role as Chair of the IABSE Task Group on uncertainties in bridge inspection and monitoring, bringing together structural engineering, sensing, and probabilistic methods.

I am looking for motivated **MSc students**, **PhD students** and **postdoctoral researchers** to join my group.

</section>

<section class="section" markdown="1">

## What's new

{% assign pub_news = site.data.publications | sort: "date" | reverse | slice: 0, 5 %}
{% assign serv_news = site.data.service | sort: "date" | reverse | slice: 0, 5 %}
{% assign talk_news = site.data.talk | sort: "date" | reverse | slice: 0, 5 %}
{% assign news = pub_news | concat: serv_news | sort: "date" | reverse | slice: 0, 5 %}
{% for item in news %}
{%- if item.title -%}
- **{{ item.date | replace: "-", "." }}** {% if item.venue == "arxiv" %}[arxiv]{% else %}[**{{ item.venue }}{% if item.award %} — {{ item.award }}{% endif %}**]{% endif %}{% if item.link %} [*"{{ item.title }}"*]({{ item.link }}){% else %} *"{{ item.title }}"*{% endif %}{% if item.status %} ({{ item.status }}){% endif %}.
{%- else -%}
- **{{ item.date | replace: "-", "." }}** {{ item.text }}
{%- endif %}
{% endfor %}

</section>

<!-- <section class="section" markdown="1">

## Awards & recognition
- **2026** NWO Talent Programme VENI.
- **2025** IABSE Best PhD Thesis.
- **2024** Marie Skłodowska-Curie Fellowship.
- **2022** EWGAE Honorable Student Paper.
- **2015-2017** TU Delft Excellent Full Scholarship.

</section> -->

<!-- <section class="section" markdown="1">

## Experience

- **2024.9–present** Assistant Professor, Delft University of Technology, the Netherlands.
- **2024.1-2024.8** MSCA Fellow, University of Cambridge, UK.
- **2022.10-2023.12** Postdoctoral researcher, Delft University of Technology, the Netherlands.

</section> -->

<!-- <section class="section" markdown="1">

## Education

- **2017.10–2022.9** PhD, Delft University of Technology, the Netherlands.
- **2015.9-2017.9** MSc, Delft University of Technology, the Netherlands.
- **2011.9-2015.6** BSc, Tongji University, China.

</section> -->

<section class="section" markdown="1">

## Research interests

- Multi-physical sensing (ultrasonics, acoustics, optics and etc.)
- Concrete deterioration (reinforcement corrosion, concrete cracking)
- Concrete structural modeling (analytical and numerical models)
- Probabilistic modeling and structural reliability (Bayesian inference, uncertainty quantification)

</section>
