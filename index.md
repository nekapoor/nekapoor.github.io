---
layout: post          # use the normal post layout so it looks like an article
title: "Welcome"
permalink: /          # makes this the root URL
---

---

## All articles

{% comment %}=============================================================
  Loop through every post and print them as an unordered list.
  `relative_url` keeps links working if you later add `baseurl`.
 ============================================================== {% endcomment %}

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <small>— {{ post.date | date: "%B %d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>