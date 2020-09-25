---
title: "Meetings"
layout: textlay
excerpt: "AI Chair OceaniX - Meetings"
sitemap: false
permalink: /meetings
---

# Webinars
(For a more detailed list of publications of AI Chair OceaniX <!--full list see [below](#full-list) or--> go to [Google Scholar](https://scholar.google.ch/citations?user=0donG7gAAAAJ), [ResearchGate](https://www.researchgate.net/profile/Ronan_Fablet))

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


