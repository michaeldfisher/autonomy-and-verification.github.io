---
layout: page
title: Contact
---

We welcome opportunities for collaboration and media engagement.

For more information please contact [Prof. Michael Fisher](http://cgi.csc.liv.ac.uk/~michael/), who is the head of the lab.

You can also keep up with our activities on twitter  <a href="https://twitter.com/{{ site.twitter_user }}">
  <i class="fa fa-twitter-square fa-2x"></i> @{{ site.twitter_user }}</a>, <a href="https://www.researchgate.net/lab/{{ site.researchgate_username }}">
    <img alt="researchgate logo" src="/images/logos/RG_square_green.png" width="32" height="32" /> research gate</a>, and <a href="https://github.com/autonomy-and-verification-uol">
    <img alt="github logo" src="/images/logos/githubcontactlogo.png" width="32" height="32" /> GitHub</a>.

<section class="columns large-4">
<div markdown="1">
<br/>
<br/>
<br/>
<br/>
## Address
**Autonomy and Verification Laboratory**  
University of Liverpool  
Department of Computer Science  
Ashton Building, Room 1.17  
Ashton Street  
Liverpool  
L69 3BX  
United Kingdom  
Phone: +44 0151 795 4237  
</div>
</section>

<section class="columns large-8">
<div markdown="1">
<section id="map" class="map">
  <iframe id="map_iframe"
    width="100%"
    height="100%"
    frameborder="0"
    scrolling="no"
    marginheight="0"
    marginwidth="0"
    src="https://maps.google.com/maps/embed/v1/place?key={{ site.google_api_key }}&q={% for address in site.address %}{{ address.line }},{% endfor %}"
    allowfullscreen>
  </iframe>
  <br>
  <small id="map_iframe"
    width="100%"
    height="100%"
    frameborder="0"
    scrolling="no"
    marginheight="0"
    marginwidth="0"
    src="https://maps.google.com/maps/embed/v1/place?key={{ site.google_api_key }}&q={% for address in site.address %}{{ address.line }},{% endfor %}"
    allowfullscreen>
  </small>
</section>
</div>
</section>
