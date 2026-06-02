---
title: siyuan-notes
---

## ?????

<div class="note-list">
{% assign notes = site.pages | where_exp: "item", "item.path contains 'content/posts/'" | sort: "date" | reverse %}
{% for note in notes %}
{% if note.path contains '/index.md' %}
<a class="note-card" href="{{ note.url | relative_url }}">
  <span>{{ note.title | default: note.path }}</span>
  <small>{% if note.date %}{{ note.date | date: "%Y-%m-%d" }}{% else %}??{% endif %}</small>
</a>
{% endif %}
{% endfor %}
</div>
