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
- {{ video.title }}: <strong><a href="{{ video.url }}">{{ video.display }}</a></strong>

{% endfor %}


