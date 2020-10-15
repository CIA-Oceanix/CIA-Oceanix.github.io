---
title: "Webinar"
layout: textlay
excerpt: "AI Chair OceaniX - Webinar"
sitemap: false
permalink: /webinar
---

# Webinars

In the context of AI Chair Oceanix, monthly webinars are proposed every third Wednesday of the month, starting in October 2020. Below are listed all the previous and coming webinars. When possible, additional links with a video record of the webinar will be provided.

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


