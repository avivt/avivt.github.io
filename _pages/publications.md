---
title: "Aviv Tamar - Publications"
layout: gridlay
excerpt: "Aviv Tamar -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

## Highlights

(For a full list see [below](#full-list) or go to [Google Scholar](https://scholar.google.co.il/citations?hl=en&user=kppa2vgAAAAJ&view_op=list_works&sortby=pubdate))

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>

## Full List

## Pre-prints

{% assign i = 0 %}
{% for publi in site.data.publist %}
{% if publi.preprint == 1 %}
  
  {% assign i = i | plus:1 %}
  {{i}}. {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endif %}
{% endfor %}

## Journal Papers

{% for publi in site.data.publist %}
{% if publi.journal == 1 %}

  {% assign i = i | plus:1 %}
  {{i}}. {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endif %}
{% endfor %}

## Conference Papers

{% for publi in site.data.publist %}
{% if publi.conference == 1 %}

  {% assign i = i | plus:1 %}
  {{i}}. {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endif %}
{% endfor %}

## Workshop Papers / Technical Reports

{% for publi in site.data.publist %}
{% if publi.workshop == 1 %}

  {% assign i = i | plus:1 %}
  {{i}}. {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endif %}
{% endfor %}
