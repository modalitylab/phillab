---
title: "PhilLab - Publications"
layout: gridlay
excerpt: "PhilLab -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

## Highlights

(For a full list see [below](#full-list) or go to [Google Scholar](https://scholar.google.com/citations?user=iwf2IBwAAAAJ&hl=en), [Publons](https://publons.com/researcher/1245235/jonathan-phillips/))

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
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="45%" style="float: left" />
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

{% for publi in site.data.publist %}

  <b>{{ publi.title }}</b> <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a><br />{{ publi.news2 }}

{% endfor %}

