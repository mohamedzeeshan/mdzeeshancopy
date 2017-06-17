---
layout: page
title: Publications
permalink: /publications/
---

<ul class="listing">
{% for post in site.posts %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
    <li class="listing-seperator">{{ y }}</li>
  {% endif %}
  <li class="listing-item">
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
    <a href="{{ post.url | prepend: site.baseurl }}" title="{{ post.title }}">{{ post.title }}</a>
    <p style="font-size: 20px; margin-bottom: 0">{{ post.snippet }}</p>
    <a href="{{ post.url | prepend: site.baseurl }}" style="font-size: 18px" title="{{ post.title }}"><i>Continue reading &rarr;</i></a>
  </li>
{% endfor %}
</ul>
