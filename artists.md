---
layout: page
title: Artist Index
category: page
artist: mwm
image: mwm-social-square
permalink: /artists/
---
<table id="artist-table">
{% for post in site.posts %}
  <tr class="index-{{ post.category }}-row">
    <td><a href="{{ post.permalink }}"><span class="index-{{ post.category }}">{{ post.category | capitalize }}: </span>{{ post.title }}</a></td>
    <td>{% if post.front_page %}Featured Content{% endif %}</td>
    <td>{{ post.date | date: '%B %d, %Y' }}</td>
  </tr>
{% endfor %}
</table>
