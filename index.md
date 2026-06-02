---
title: siyuan-notes
---

<div class="home-intro">
  <h2>&#24050;&#21457;&#24067;&#31508;&#35760;</h2>
  <p>&#36825;&#37324;&#20250;&#33258;&#21160;&#27719;&#24635;&#21457;&#24067;&#21040; <code>content/posts</code> &#30340;&#24605;&#28304;&#31508;&#35760;&#12290;</p>
</div>

<div class="article-list" id="notes">
{% assign notes = site.pages | where_exp: "item", "item.path contains 'content/posts/'" | sort: "date" | reverse %}
{% assign count = 0 %}
{% for note in notes %}
{% if note.path contains '/index.md' %}
{% assign count = count | plus: 1 %}
<a class="article-card" href="{{ note.url | relative_url }}">
  <div class="article-card-body">
    <h3>{{ note.title | default: note.path }}</h3>
    <p>{{ note.content | strip_html | strip_newlines | truncate: 120 }}</p>
    <div class="article-meta">{% if note.date %}{{ note.date | date: "%Y-%m-%d" }}{% else %}Note{% endif %}</div>
  </div>
  <div class="article-thumb">{{ note.title | default: 'N' | slice: 0, 1 }}</div>
</a>
{% endif %}
{% endfor %}
{% if count == 0 %}
<p class="empty-state">&#26242;&#26080;&#24050;&#21457;&#24067;&#31508;&#35760;&#12290;</p>
{% endif %}
</div>