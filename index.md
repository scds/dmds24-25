---
layout: home
title: Home
description: DMDS Webinars
nav_order: 1
---

{%- assign workshops = site.pages 
    | where_exp: "item", "item.grand_parent == null"
    | where_exp: "item", "item.parent == null"
    | sort: "title" 
-%}

<img src="assets/img/titleSlide.png" alt="Workshop Title Slide" width="100%">

# Welcome to the 2024-2025 Do More with Digital Scholarship Webinars

What is digital scholarship, how can I do more with it, and how can it contribute to my research and teaching? Join us for our free workshop series that introduces McMaster students, faculty, and staff to the multifaceted domain of digital scholarship.

Join us to: 
- Develop skills for professionalization.
- Learn to use software to create digital exhibits, perform data analysis and create dashboards, and organize your research images.
- Engage with faculty, staff, and students on a wide range of topics.
- Learn more about digital approaches to research and knowledge mobilization.
- Explore the intersections between digital scholarship and critical humanities; cybersecurity and data justice. 

## 2024-25 DMDS Workshops

<div markdown="1" style="border: 1px solid #7a003c; border-radius: 6px; margin-bottom: 1em; padding: 0.5em 1em 0; margin-top: 1em;" class="toc">
<summary style="cursor:default; display: block; border-bottom: 1px solid #302d36; margin-bottom: 0.5em">
  Workshops
</summary>
<ul>
{% for workshop in workshops %}
{% if workshop.title != null and workshop.title != "Home" %}
<li><a href="{{workshop.url | absolute_url}}">{{workshop.title}}</a></li>
{% endif %}
{% endfor %}
</ul>
</div>
