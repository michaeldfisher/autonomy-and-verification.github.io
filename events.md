---
layout: page
title: Events
---

Upcoming Workshops, Tutorials, and other events run by [Members](/members) of the Autonomy and Verification Lab.

<section >
  <ul>
    {% for event in site.events  %}
      <li>
        <a href="{{ site.url }}{{ event.url }}">{% if site.titlecase %}{{ event.title | titlecase }}{% else %}{{ event.title }}{% endif %}</a>
      </li>
    {% endfor %}
  </ul>
</section>
