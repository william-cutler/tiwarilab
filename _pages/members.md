---
title: "Goodwill Lab - Group members"
layout: gridlay
excerpt: "Goodwill Lab: Group members"
sitemap: false
permalink: /members/
---
# Group Members

### Principal Investigator

<div class="row">
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ site.data.team_members.pi.photo }}" class="img-responsive" style="float: left; border-radius: 50%; height: 100px; width: 100px; object-fit: cover; overflow: hidden;" />
  <h4>{{ site.data.team_members.pi.name }}</h4>
  
  <i>{{ site.data.team_members.pi.email }}</i>
</div>
</div>

{% for student_group in site.data.team_members.student_categories %}

  <h3>{{ student_group.text }}</h3>

{% assign number_printed = 0 %}
{% for member in student_group.individuals %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}

  <div class="row">
  {% endif %}
  <div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" style="float: left; border-radius: 50%; height: 100px; width: 100px; object-fit: cover; overflow: hidden;" />
  <h4>{{ member.name }}</h4>
  {% if member.webpage == nil %}
  <a href="{{ site.url }}{{ site.baseurl }}/" style="color: red;">Home Page</a>
  {% else %}
  <a href="{{ member.webpage }}" style="color: blue;">Home Page</a>
  {% endif %}
  <i>{{ member.email }}</i>
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
{% endfor %}


### Goodwill Lab Friends

<div class="row">

<div class="col-sm-5 clearfix">
{% for member in site.data.team_members.friends %}
<b>{{ member.name }}</b>, {{member.info}}
{% endfor %}
</div>

</div>
