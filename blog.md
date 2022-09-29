---
layout: page
title: Blog
permalink: /blog/
bgimage: /assets/images/ASOP_AltarRock_Sept2022_12.jpg
---

<div class="container">
    
{% for post in site.posts %}
{% assign indexmod3 = forloop.index | modulo: 3 %}
{% if indexmod3 == 1 %}<div class="row">{% endif %}

<div class="col-12 col-md-6 col-lg-4 blog-item">

<a href="{{ post.url }}"><img src="{{ post.bgimage | relative_url }}" class="img-responsive" alt="{{ post.image-title }}"/></a>
<h3 class="blog-title"><a href="{{ post.url }}">{{ post.title }}</a></h3>
<span>{{ post.date | date_to_string }}</span>
<!--{{ post.excerpt }}-->
</div>

{% if indexmod3 == 0 %}</div>{% endif %}
{% endfor %}

</div>


