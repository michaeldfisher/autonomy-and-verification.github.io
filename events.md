---
layout: page
title: Events
---

Upcoming Events by Members of the A&V Lab

<section >
  <ul>
    {% for event in site.events  %}
      <li>
        <a href="{{ site.url }}{{ event.url }}">{% if site.titlecase %}{{ event.title | titlecase }}{% else %}{{ event.title }}{% endif %}</a>
      </li>
    {% endfor %}
  </ul>
</section>
