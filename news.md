---
layout: default
---

**[Home](.)** | **[People](people.md)** | **[Teaching](teaching.md)** | **[Publications](publications.md)** | **[News](news.md)** | **[Contact](contact.md)**

---

# Lab News

Here are our latest updates:

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a> ({{ post.date | date: "%B %d, %Y" }})
    </li>
  {% endfor %}
</ul>
