---
title: "OceaniX Videos"
layout: gridlay
excerpt: "AI Chair OceaniX - Videos"
sitemap: false
permalink: /oceanix_video
---

# Recorded OceaniX Videos and Talks

<!--{% assign number_printed = 0 %} -->
{% for video in site.data.video_list %}
<li> <pubtit>{{ video.title }}</pubtit>: <p><strong><a href="{{ video.url }}">{{ video.display }}</a></strong></p> 
  </li>
{% endfor %}


