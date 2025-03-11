---
layout: page
title: Home
id: home
permalink: /
---

# Xin chào đến khu vườn của mình 🌱

Đây là trang web mình thử nghiệm với Jerkill

<strong>Bài viết mới gần đây</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
