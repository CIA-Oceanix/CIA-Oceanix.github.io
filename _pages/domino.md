---
title: "Domino"
layout: textlay
excerpt: "AI Chair OceaniX - Domino"
sitemap: false
permalink: /domino
---

# Domino

Domino is...

## List of previous Domino session

{% assign number_printed = 0 %}
{% for domino in site.data.dominolist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if domino.highlight == 1 %}
{% if domino.codetype == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ domino.title }}</pubtit>
  <p>{{ domino.date }} <br></p>
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ domino.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ domino.description }}</p>
  <p><em>{{ domino.authors }}</em></p>
  <p><strong><a href="{{ domino.link.url }}">{{ domino.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ domino.news1 }}</strong></p>
  <p> {{ domino.news2 }}</p>
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

## List of coming Domino session

{% assign number_printed = 0 %}
{% for domino in site.data.dominolist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if domino.highlight == 1 %}
{% if domino.codetype == 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ domino.title }}</pubtit>
  <p>{{ domino.date }} <br> </p>
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ domino.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ domino.description }}</p>
  <p><em>{{ domino.authors }}</em></p>
  <p><strong><a href="{{ domino.link.url }}">{{ domino.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ domino.news1 }}</strong></p>
  <p> {{ domino.news2 }}</p>
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


