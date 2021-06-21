---
title: "CCCN2021 Poster rooms"
layout: cccn2021
excerpt: "CCCN2021 Poster rooms"
sitemap: false
permalink: /cccn2021/poster_room
---

# CCCN2021 Poster session

*[Main site](https://meeting.cns.org.cn/2021CCCN/)*.

**Poster session time:** 2021-06-11 18:10-21:00 Beijing Time(UTC+8).

<br />

{% assign number_printed = 0 %}
{% for publi in site.data.cccn2021_posters_preview %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>分组编号： {{ publi.ID }} <a href="{{ site.url }}{{ site.baseurl }}/cccn2021/poster/{{ publi.poster }}">[Poster]</a></pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/cccn2021_poster_preview/{{ publi.preview }}" class="img-responsive" width="33%" style="float: left" />
  <p></p>
  <p><em>{{ publi.authors }}</em></p>
  <p>{{ publi.affiliation }}</p>
  <p></p>
  <br />
  <br />
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

