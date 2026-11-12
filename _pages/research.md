---
layout: page
title: Research
permalink: /research/
nav: true
nav_order: 1
description: Seismic waves as a window into Earth's structure, from the crust to the deep mantle.
---

My research brings together numerical simulations and seismic observations to understand which parts of a waveform carry useful structural information, and how we can use that information in an inversion.

<div class="research-index" aria-label="Research projects">
{% assign projects = site.projects | sort: 'importance' %}
{% for project in projects %}
<article class="research-card">
<div class="project-meta"><span>{{ project.topic }}</span><span class="project-status">{{ project.status }}</span></div>
<h2><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h2>
<p>{{ project.description }}</p>
<a class="project-link" href="{{ project.url | relative_url }}">Explore project</a>
</article>
{% endfor %}
</div>
