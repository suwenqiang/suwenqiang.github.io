---
layout: default
title: Home
---

## Personal Knowledge Base

Use this site to record recurring problems, root-cause analysis, and the fixes that are easy to forget after a few weeks.

### How To Use This Site

- Write long-lived reference notes under topic folders such as `android/`, `linux/`, and `network/`.
- Write time-based troubleshooting logs under `_posts/`.
- Tag posts with categories so they automatically appear on the corresponding topic page.

### Topic Areas

<div class="note-grid">
  <a class="note-card" href="/android/">
    <h3>Android</h3>
    <p>ADB, build issues, flashing, debugging, permissions, and device bring-up notes.</p>
  </a>
  <a class="note-card" href="/linux/">
    <h3>Linux</h3>
    <p>Shell, package management, SSH, Git, system services, and workstation setup notes.</p>
  </a>
  <a class="note-card" href="/network/">
    <h3>Network</h3>
    <p>DNS, proxies, VPN, routing, connectivity issues, and environment-specific network fixes.</p>
  </a>
</div>

### Recent Troubleshooting Logs

{% if site.posts.size > 0 %}
<ul class="note-list">
  {% for post in site.posts limit: 8 %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
    <span class="note-meta">{{ post.date | date: "%Y-%m-%d" }}</span>
  </li>
  {% endfor %}
</ul>
{% else %}
No troubleshooting logs yet. Add a Markdown file under `_posts/` to start tracking fixes.
{% endif %}

### Suggested Note Template

```md
---
layout: page
title: "Problem title"
permalink: /topic/problem-path/
---

## Symptom

## Environment

## Root Cause

## Fix

## Verification

## Keywords
```
