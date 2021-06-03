---
title: "CCCN2021 Poster rooms"
layout: cccn2021
excerpt: "CCCN2021 Poster rooms"
sitemap: false
permalink: /cccn2021/poster_room
---

# CCCN2021 Poster rooms

{% assign number_printed = 0 %}
{% for publi in site.data.cccn2021_posters %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <p><em>{{ publi.authors }}</em></p>
  <p>Room ID: <a href="{{ publi.entrance.link }}">{{ publi.entrance.ID }}</a></p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>

