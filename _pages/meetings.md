---
title: "Meetings"
layout: textlay
excerpt: "AI Chair OceaniX - Meetings"
sitemap: false
permalink: /meetings
---

Link to OceaniX calendar with all scheduled events and meetings: [here](https://calendar.google.com/calendar/embed?src=8kceabbp1iv27a02sb673u18uc%40group.calendar.google.com&ctz=Europe%2FParis)

# Webinars

In the context of AI Chair Oceanix and AI4OAC project, we organize a webinar every third Wednesday of the month, starting in October 2020. When possible, additional links with a video record of the webinar will be provided.

## List of previous Webinars

{% assign number_printed = 0 %}
{% for webinar in site.data.webinarlist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if webinar.highlight == 1 %}
{% if webinar.codetype == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ webinar.title }}</pubtit>
  <p>{{ webinar.date }} <br></p>
  <img src="{{ site.url }}{{ site.baseurl }}/images/webinarpic/{{ webinar.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ webinar.description }}</p>
  <p><em>{{ webinar.authors }}</em></p>
  <p><strong><a href="{{ webinar.link.url }}">{{ webinar.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ webinar.news1 }}</strong></p>
  <p> {{ webinar.news2 }}</p>
  <p><strong><a href="{{ webinar.recordlink.url }}">{{ webinar.recordlink.display }}</a></strong></p>
  <p><strong><a href="{{ webinar.slideslink.url1 }}">{{ webinar.slideslink.display1 }}</a></strong></p>
  <p><strong><a href="{{ webinar.slideslink.url2 }}">{{ webinar.slideslink.display2 }}</a></strong></p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>

## List of coming Webinars

{% assign number_printed = 0 %}
{% for webinar in site.data.webinarlist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if webinar.highlight == 1 %}
{% if webinar.codetype == 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ webinar.title }}</pubtit>
  <p>{{ webinar.date }} <br> </p>
  <img src="{{ site.url }}{{ site.baseurl }}/images/webinarpic/{{ webinar.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ webinar.description }}</p>
  <p><em>{{ webinar.authors }}</em></p>
  <p><strong><a href="{{ webinar.link.url }}">{{ webinar.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ webinar.news1 }}</strong></p>
  <p> {{ webinar.news2 }}</p>
  <p><strong><a href="{{ webinar.zoomlink.url }}">{{ webinar.zoomlink.display }}</a></strong></p>
  <p> {{ webinar.zoomlink.ID }}</p>
  <p> {{ webinar.zoomlink.Passcode }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


