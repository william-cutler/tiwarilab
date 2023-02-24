---
title: "Goodwill Lab - Group members"
layout: gridlay
excerpt: "Goodwill Lab: Group members"
sitemap: false
permalink: /members/
---


## Principal Investigator
<div class="row">
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ site.data.team_members.pi.photo }}" class="img-responsive" width="30%" style="float: left" />
  <h4>{{ site.data.team_members.pi.name }}</h4>
  
  <i>{{ site.data.team_members.pi.email }}</i>
</div>
</div>

## PhD Thinkers
{% assign number_printed = 0 %}
{% for member in site.data.team_members.phd %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="30%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <a href="{{member.webpage}}" style="color: blue;">{{member.webpage}}</a>
  <i> <br> {{ member.email }}</i>
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

## Undergrad Explorers
{% assign number_printed = 0 %}
{% for member in site.data.team_members.undergrad %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="30%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <a href="{{member.webpage}}" style="color: blue;">{{member.webpage}}</a>
  <i> <br> {{ member.email }}</i>
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

## Goodwill Lab Friends
<div class="row">

<div class="col-sm-4 clearfix">
{% for member in site.data.team_members.friends %}
<b>{{ member.name }}</b>, {{member.info}}
{% endfor %}
</div>

</div>
