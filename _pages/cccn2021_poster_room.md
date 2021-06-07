---
title: "CCCN2021 Poster rooms"
layout: cccn2021
excerpt: "CCCN2021 Poster rooms"
sitemap: false
permalink: /cccn2021/poster_room
---

# CCCN2021 Poster session

*[Main site](https://meeting.cns.org.cn/2021CCCN/)*.

**Poster session time:** 2021-06-13 09:00-12:00 Beijing Time(UTC+8).

<br />

{% assign number_printed = 0 %}
{% for publi in site.data.cccn2021_posters %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }} <a href="{{ publi.abstract }}">[Abstract]</a></pubtit>
  <p></p>
  <p><em>{{ publi.authors }}</em></p>
  <p>{{ publi.affiliation }}</p>
  <p>Keywords: {{ publi.keywords }}</p>
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

