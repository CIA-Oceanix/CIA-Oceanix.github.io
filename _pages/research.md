---
title: "AI Chair OceaniX - Code & Datasets"
layout: textlay
excerpt: "AI Chair OceaniX - Code & Datasets"
sitemap: false
permalink: /research/
---

# Codes and Datasets

All OceaniX shared codes and datasets are availabe on our github repo [here](https://github.com/CIA-Oceanix). Some highlights below.

## Code highlights
{% assign number_printed = 0 %}
{% for code in site.data.codelist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if code.highlight == 1 %}
{% if code.codetype == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ code.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ code.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ code.description }}</p>
  <!--<p><em>{{ code.authors }}</em></p>-->
  <p>Associated paper:<strong><a href="{{ code.paper.url }}">here</a></strong></p>
  <p><strong><a href="{{ code.link.url }}">{{ code.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ code.news1 }}</strong></p>
  <p> {{ code.news2 }}</p>
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


## Dataset highlights
{% assign number_printed = 0 %}
{% for code in site.data.codelist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if code.highlight == 1 %}
{% if code.codetype == 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ code.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ code.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ code.description }}</p>
  <!--<p><em>{{ code.authors }}</em></p>-->
  <p>Associated paper:<strong><a href="{{ code.paper.url }}">here</a></strong></p>
  <p><strong><a href="{{ code.link.url }}">{{ code.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ code.news1 }}</strong></p>
  <p> {{ code.news2 }}</p>
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


## Full list of available codes
{% for code in site.data.codelist %}
{% if code.codetype == 1 %}
{{ code.title }} <strong><a href="{{ code.link.url }}">{{ code.link.display }}</a></strong>
{% endif %}
{% endfor %}

## Full list of available datasets
{% for code in site.data.codelist %}
{% if code.codetype == 2 %}
{{ code.title }} <strong><a href="{{ code.link.url }}">{{ code.link.display }}</a></strong>
{% endif %}
{% endfor %}

