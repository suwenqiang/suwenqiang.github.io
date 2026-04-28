---
layout: page
title: Network Notes
permalink: /network/
---

Reference notes and troubleshooting logs related to DNS, proxies, VPNs, and connectivity issues.

## Reference Notes

- [Proxy Troubleshooting Checklist](/network/proxy-troubleshooting-checklist/)

## Related Posts

{% assign notes = site.posts | where_exp: "post", "post.categories contains 'network'" %}
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
No network troubleshooting posts yet.
{% endif %}
