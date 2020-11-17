---
title: "OceaniX Sandbox"
layout: textlay
excerpt: "AI Chair OceaniX - Sandbox"
sitemap: false
permalink: /oceanix_sandbox
---

# OceaniX Sandbox

You can find here all the informations and presentations of interest from Friday morning OceaniX team meetings.


## Upcoming sessions


{% assign number_printed = 0 %}
{% for oceanix_sandbox in site.data.oceanix_sandboxlist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if oceanix_sandbox.highlight == 1 %}
{% if oceanix_sandbox.codetype == 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ oceanix_sandbox.title }}</pubtit>
  <p>{{ oceanix_sandbox.date }} <br> </p>
  <img src="{{ site.url }}{{ site.baseurl }}/images/sandbox_pic/{{ oceanix_sandbox.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ oceanix_sandbox.description }}</p>
  <p><em>{{ oceanix_sandbox.authors }}</em></p>
  <p><strong><a href="{{ oceanix_sandbox.link.url }}">{{ oceanix_sandbox.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ oceanix_sandbox.news1 }}</strong></p>
  <p> {{ oceanix_sandbox.news2 }}</p>
  <p><strong><a href="{{ oceanix_sandbox.zoomlink.url }}">{{ oceanix_sandbox.zoomlink.display }}</a></strong></p>
  <p> {{ oceanix_sandbox.zoomlink.ID }}</p>
  <p> {{ oceanix_sandbox.zoomlink.Passcode }}</p>
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

## Previous meetings

{% assign number_printed = 0 %}
{% for oceanix_sandbox in site.data.sandbox_list %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if oceanix_sandbox.highlight == 1 %}
{% if oceanix_sandbox.codetype == 1 %}

{% if even_odd == 0 &%}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ oceanix_sandbox.title }}</pubtit>
  <p>{{ oceanix_sandbox.date }} <br></p>
  <img src="{{ site.url }}{{ site.baseurl }}/images/sandbox_pic/{{ oceanix_sandbox.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ oceanix_sandbox.description }}</p>
  <p><em>{{ oceanix_sandbox.authors }}</em></p>
  <p><strong><a href="{{ oceanix_sandbox.link.url }}">{{ oceanix_sandbox.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ oceanix_sandbox.news1 }}</strong></p>
  <p> {{ oceanix_sandbox.news2 }}</p>
  <p><strong><a href="{{ oceanix_sandbox.recordlink.url }}">{{ oceanix_sandbox.recordlink.display }}</a></strong></p>
  <p><strong><a href="{{ oceanix_sandbox.slideslink.url1 }}">{{ oceanix_sandbox.slideslink.display1 }}</a></strong></p>
  <p><strong><a href="{{ oceanix_sandbox.slideslink.url2 }}">{{ oceanix_sandbox.slideslink.display2 }}</a></strong></p>
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


