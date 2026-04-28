---
layout: note
title: Linux Notes
permalink: /linux/
---

Reference notes and troubleshooting logs for local workstation setup, shell behavior, Git, SSH, and package management.

## Reference Notes

- [Git Push Ref Mapping Check](/linux/git-push-ref-mapping-check/)

## Related Posts

{% assign notes = site.posts | where_exp: "post", "post.categories contains 'linux'" %}
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
No Linux troubleshooting posts yet.
{% endif %}
