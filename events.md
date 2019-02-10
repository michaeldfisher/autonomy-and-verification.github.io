---
layout: page
title: Events
---

Upcoming Workshops, Tutorials, and other events run by [Members](/members) of the Autonomy and Verification Lab.

<article class="row">

<section class="columns large-7" >
<h2>Events</h2>
  <ul>
    {% for event in site.events  %}
      {% if event.series != true and event.date >= site.time %}
      <li>
        [{{ event.date | date: "%-d %B %Y" }}] <a href="{{ site.url }}{{ event.url }}">{% if site.titlecase %}{{ event.title | titlecase }}{% else %}{{ event.title }}{% endif %}</a>
      </li>
      {% endif %}
    {% endfor %}
  </ul>

<h2>Past Events</h2>
<ul>
  {% for event in site.events  %}
    {% if event.series != true  and event.date < site.time %}
    <li>
      [{{ event.date | date: "%-d %B %Y" }}] <a href="{{ site.url }}{{ event.url }}">{% if site.titlecase %}{{ event.title | titlecase }}{% else %}{{ event.title }}{% endif %}</a>
    </li>
    {% endif %}
  {% endfor %}
</ul>


</section>

<section class="columns large-3" >
<h2>Event Series</h2>
<ul>
  {% for event in site.events  %}
    {% if event.series == true %}
    <li>
       <a href="{{ site.url }}{{ event.url }}">{% if site.titlecase %}{{ event.title | titlecase }}{% else %}{{ event.title }}{% endif %}</a>
    </li>
    {% endif %}
  {% endfor %}
</ul>
</section>

</article>
