---
layout: page
title: Content Archive
category: page
artist: mwm
image: mwm-social-square
permalink: /archive/
seo_description: There's a lot of content not featured on the front page. Look around and enjoy!
seo_keywords: weird music, unique music, progressive rock, jazz, prog, composition
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
