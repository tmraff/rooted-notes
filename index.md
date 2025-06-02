---
layout: page
title: Rooted Notes
permalink: /
---

## Garden Index

- Garden Map — you are here
- [About](about) — a quiet introduction to who I am and what this is
- [Essays](essays-collection/) — arguments, observations, philosophical inquiries
- [Fiction](fiction-collection/) — weird horror, strange devotion, queer magic
- [Seasons](seasons-collection/) — what I’m working on, reading, and growing each quarter
- [Templates](templates-collection/) — free reusable markdown structures for digital gardening
- [Posts](posts/) — pieces that don’t quite belong anywhere else
- [Drafts](drafts/) — private, but real; the structure beneath everything
- [License](license) — rights, permissions, and creative commons


{% assign all_notes = site.essays | concat: site.fiction | concat: site.seasons | concat: site.templates %}

## Taxonomy

### Roots

Foundational ideas that ground Rooted Notes.

{% assign roots = all_notes | where_exp: "note", "note.tags contains 'roots'" | sort: "date" | reverse %}
{% for note in roots limit:3 %}
<div class="note-preview">
  {% if note.image %}
    <a href="{{ note.url | relative_url }}">
      <img src="{{ note.image | relative_url }}" alt="" class="note-thumbnail">
    </a>
  {% endif %}

  <h3><a href="{{ note.url | relative_url }}">{{ note.title }}</a></h3>

  {% if note.date %}
    <p class="note-date">{{ note.date | date: "%-d %B %Y" }}</p>
  {% endif %}

  <p>{{ note.excerpt | markdownify }}</p>

  <p><a href="{{ note.url | relative_url }}">Read more →</a></p>
</div>
{% endfor %}
<p><a href="tags/roots/">See all roots →</a></p>

### Shoots

New questions, explorations, theories.

{% assign shoots = all_notes | where_exp: "note", "note.tags contains 'shoots'" | sort: "date" | reverse %}
{% for note in shoots limit:3 %}
<div class="note-preview">
  {% if note.image %}
    <a href="{{ note.url | relative_url }}">
      <img src="{{ note.image | relative_url }}" alt="" class="note-thumbnail">
    </a>
  {% endif %}

  <h3><a href="{{ note.url | relative_url }}">{{ note.title }}</a></h3>

  {% if note.date %}
    <p class="note-date">{{ note.date | date: "%-d %B %Y" }}</p>
  {% endif %}

  <p>{{ note.excerpt | markdownify }}</p>

  <p><a href="{{ note.url | relative_url }}">Read more →</a></p>
</div>
{% endfor %}
<p><a href="tags/shoots/">See all shoots →</a></p>

### Entanglements

Contradictions, arguments with older notes.

{% assign entanglements = all_notes | where_exp: "note", "note.tags contains 'entanglements'" | sort: "date" | reverse %}
{% for note in entanglements limit:3 %}
<div class="note-preview">
  {% if note.image %}
    <a href="{{ note.url | relative_url }}">
      <img src="{{ note.image | relative_url }}" alt="" class="note-thumbnail">
    </a>
  {% endif %}

  <h3><a href="{{ note.url | relative_url }}">{{ note.title }}</a></h3>

  {% if note.date %}
    <p class="note-date">{{ note.date | date: "%-d %B %Y" }}</p>
  {% endif %}

  <p>{{ note.excerpt | markdownify }}</p>

  <p><a href="{{ note.url | relative_url }}">Read more →</a></p>
</div>
{% endfor %}
<p><a href="tags/entanglements/">See all entanglements →</a></p>

### Compost

Ideas abandoned, evolved past, or left to nourish others.

{% assign compost = all_notes | where_exp: "note", "note.tags contains 'compost'" | sort: "date" | reverse %}
{% for note in compost limit:3 %}
<div class="note-preview">
  {% if note.image %}
    <a href="{{ note.url | relative_url }}">
      <img src="{{ note.image | relative_url }}" alt="" class="note-thumbnail">
    </a>
  {% endif %}

  <h3><a href="{{ note.url | relative_url }}">{{ note.title }}</a></h3>

  {% if note.date %}
    <p class="note-date">{{ note.date | date: "%-d %B %Y" }}</p>
  {% endif %}

  <p>{{ note.excerpt | markdownify }}</p>

  <p><a href="{{ note.url | relative_url }}">Read more →</a></p>
</div>
{% endfor %}

<p><a href="tags/compost/">See all compost →</a></p>

### Wildflowers

Fiction, poetry, art, strange experiments.

{% assign wildflowers = all_notes | where_exp: "note", "note.tags contains 'wildflowers'" | sort: "date" | reverse %}
{% for note in wildflowers limit:3 %}
<div class="note-preview">
  {% if note.image %}
    <a href="{{ note.url | relative_url }}">
      <img src="{{ note.image | relative_url }}" alt="" class="note-thumbnail">
    </a>
  {% endif %}

  <h3><a href="{{ note.url | relative_url }}">{{ note.title }}</a></h3>

  {% if note.date %}
    <p class="note-date">{{ note.date | date: "%-d %B %Y" }}</p>
  {% endif %}

  <p>{{ note.excerpt | markdownify }}</p>

  <p><a href="{{ note.url | relative_url }}">Read more →</a></p>
</div>
{% endfor %}
<p><a href="tags/wildflowers/">See all wildflowers →</a></p>
