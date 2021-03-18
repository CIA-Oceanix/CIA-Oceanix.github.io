
---
title: "OceaniX Videos"
layout: gridlay
excerpt: "AI Chair OceaniX - Videos"
sitemap: false
permalink: /oceanix_video
---

# Recorded OceaniX Videos and Talks

{% assign number_printed = 0 %}
{% for oceanix_video in site.data.video_list %}
<li> <pubtit>{{ oceanix_video.title }}</pubtit>: <p><strong><a href="{{ oceanix_video.url }}">{{ oceanix_video.display }}</a></strong></p> 
  </li>



