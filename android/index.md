---
layout: page
title: Android Notes
permalink: /android/
---

Reference notes and troubleshooting logs related to Android development, flashing, debugging, and bring-up.

## Reference Notes

- [ADB Remount Checklist](/android/adb-remount-checklist/)

## Related Posts

{% assign notes = site.posts | where_exp: "post", "post.categories contains 'android'" %}
{% if notes.size > 0 %}
<ul class="note-list">
  {% for post in notes %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
    <span class="note-meta">{{ post.date | date: "%Y-%m-%d" }}</span>
  </li>
  {% endfor %}
</ul>
{% else %}
No Android troubleshooting posts yet.
{% endif %}
