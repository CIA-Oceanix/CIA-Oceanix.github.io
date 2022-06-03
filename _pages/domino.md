---
title: "Domino"
layout: gridlay
excerpt: "AI Chair OceaniX - Domino"
sitemap: false
permalink: /domino
---

# Domino

Domino is a journal club to discuss papers of interest while eating pizzas.
<!--**Zoom conference for session on Nov. 25**: [link](https://zoom.us/j/94354512890?pwd=cHNCMlVISVRnZjFuN29TV2d2a1R3UT09)-->

## Some tips on Domino sessions and reading groups: 
- **For the "Guru" to lead a Domino session**: [link](http://muratbuffalo.blogspot.fr/2015/05/how-to-run-effective-paper-reading.html)
- **For all**: [link](http://muratbuffalo.blogspot.fr/2013/07/how-i-read-research-paper.html)

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
  <img src="{{ site.url }}{{ site.baseurl }}/images/domino_pic/{{ domino.image }}" class="img-responsive" width="33%" style="float: left" />
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
  <img src="{{ site.url }}{{ site.baseurl }}/images/domino_pic/{{ domino.image }}" class="img-responsive" width="33%" style="float: left" />
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

