---
layout: page
title: Content Index
category: page
artist: mwm
image: mwm-social-square
permalink: /index/
---
The following table contains a listing of all the posts on the site.

Posts marked with <i class="fa fa-youtube-play"></i> contain a video we produced to support the content.

<table id="artist-table">
{% for post in site.posts %}
  <tr class="index-{{ post.category }}-row">
    <td><a href="{{ post.permalink }}">{% if post.front_page %}<i class="fa fa-youtube-play"></i> {% endif %}<span class="index-{{ post.category }}">{{ post.category | capitalize }}: </span>{{ post.title }}</a></td>
    <td>{{ post.date | date: '%B %Y' }}</td>
  </tr>
{% endfor %}
</table>
