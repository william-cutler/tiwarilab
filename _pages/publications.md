---
title: "Goodwill Lab - Publications"
layout: textlay
excerpt: "Goodwill Lab -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

{% for year in site.data.publications %}
  <h2>{{ year.text }}</h2>
{% for pub in year.elements %}
  <b>[{{ pub.conference}}]</b> <br/>
  <em>{{ pub.paper}}</em> <br/>
  <a href="{{ pub.link }}">{{ pub.link }}</a>

{% endfor %}
{% endfor %}
