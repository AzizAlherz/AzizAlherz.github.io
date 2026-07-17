---
layout: archive
title: "Research Group"
permalink: /group/
author_profile: true
description: "Meet the Alherz Lab team at Kuwait University — graduate and undergraduate researchers using computational chemistry and DFT to design next-generation energy materials."
---

{% include base_path %}

{% assign graduates   = site.team | where: "role", "graduate" %}
{% assign undergrads  = site.team | where: "role", "undergraduate" %}
{% assign postdocs    = site.team | where: "role", "postdoc" %}
{% assign alumni      = site.team | where: "role", "alumni" %}

The Alherz Lab is home to a diverse group of researchers united by a passion for using computational methods to solve real-world energy and sustainability challenges. We welcome motivated students at all levels.

---

## Graduate Students

{% if graduates.size > 0 %}
{% for member in graduates %}
<div style="margin-bottom: 1.5em;">
  {% if member.photo %}<img src="/images/team/{{ member.photo }}" alt="{{ member.name }}" style="width:80px; height:80px; border-radius:50%; float:left; margin-right:1em;">{% endif %}
  <strong>{{ member.name }}</strong><br>
  <em>{{ member.degree }}, {{ member.institution }}</em><br>
  <span style="color:#555;">Project: {{ member.project }}</span>
  {% if member.email %}<br><a href="mailto:{{ member.email }}">{{ member.email }}</a>{% endif %}
  <div style="clear:both;"></div>
</div>
{% endfor %}
{% else %}
*No current graduate students.*
{% endif %}

---

## Undergraduate Students

{% if undergrads.size > 0 %}
{% for member in undergrads %}
<div style="margin-bottom: 1.5em;">
  {% if member.photo %}<img src="/images/team/{{ member.photo }}" alt="{{ member.name }}" style="width:80px; height:80px; border-radius:50%; float:left; margin-right:1em;">{% endif %}
  <strong>{{ member.name }}</strong><br>
  <em>{{ member.degree }}, {{ member.institution }}</em><br>
  <span style="color:#555;">Project: {{ member.project }}</span>
  {% if member.email %}<br><a href="mailto:{{ member.email }}">{{ member.email }}</a>{% endif %}
  <div style="clear:both;"></div>
</div>
{% endfor %}
{% else %}
*No current undergraduate researchers.*
{% endif %}

---

## Postdoctoral Researchers

{% if postdocs.size > 0 %}
{% for member in postdocs %}
<div style="margin-bottom: 1.5em;">
  {% if member.photo %}<img src="/images/team/{{ member.photo }}" alt="{{ member.name }}" style="width:80px; height:80px; border-radius:50%; float:left; margin-right:1em;">{% endif %}
  <strong>{{ member.name }}</strong><br>
  <em>{{ member.institution }}</em><br>
  <span style="color:#555;">Project: {{ member.project }}</span>
  {% if member.email %}<br><a href="mailto:{{ member.email }}">{{ member.email }}</a>{% endif %}
  <div style="clear:both;"></div>
</div>
{% endfor %}
{% else %}
*No current postdoctoral researchers. Interested candidates are encouraged to [reach out](mailto:abdulaziz.alherz@ku.edu.kw).*
{% endif %}

---

## Alumni

{% if alumni.size > 0 %}
{% for member in alumni %}
<div style="margin-bottom: 1em;">
  <strong>{{ member.name }}</strong> — {{ member.degree }}, {{ member.institution }}
  {% if member.end_date %} ({{ member.end_date | date: "%Y" }}){% endif %}
  {% if member.project %}<br><span style="color:#555;">{{ member.project }}</span>{% endif %}
  {% if member.current_position %}<br><em>Now: {{ member.current_position }}</em>{% endif %}
</div>
{% endfor %}
{% else %}
*No alumni yet.*
{% endif %}

---

## Join the Lab

We are actively recruiting motivated M.S. and Ph.D. students and undergraduate research assistants. If you are interested in computational chemistry, materials discovery, or sustainable energy research, please [get in touch](mailto:abdulaziz.alherz@ku.edu.kw).
