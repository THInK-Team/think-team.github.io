---
layout: home
title: Invited Talks
permalink: /invited-talks/
description: "Talks given by Boris Vaisband about chiplet design, heterogeneous integration, and fine-pitch interconnect platforms for AI and high-performance computing systems."

---

# Invited Talks

{% assign talks = site.data.invited-talks %}

{% if talks %}
{% assign sorted_talks = talks | sort: "sort_date" | reverse %}

<ul class="invited-talks-list">
{% for talk in sorted_talks %}
{%- assign title = talk.title | strip -%}
{%- assign venue = talk.venue | strip -%}
{%- assign location = talk.location | strip -%}
{%- assign date = talk.date | strip -%}
{%- assign note = talk.note | strip -%}
<li>
    {{ talk.speaker }},{% if title.size > 0 %} “{{ title }},”{% endif %}{% if venue.size > 0 %} {{ venue }}{% endif %}{% if location.size > 0 %}, {{ location }}{% endif %}{% if date.size > 0 %}, {{ date }}{% endif %}.{% if note.size > 0 %} {{ note }}{% endif %}
    {% if talk.link %}
<a href="{{ talk.link }}">Link</a>
    {% endif %}
</li>
{% endfor %}
</ul>

{% else %}
<p>No invited talks listed yet.</p>
{% endif %}