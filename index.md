---
layout: home
title: Системное программирование ММФ НГУ
---

{% for item in site.header_pages %}
  {% assign matching_pages = site.pages | where: "path", item %}
  {% assign home_pages = home_pages | concat: matching_pages %}
{% endfor %}

{% include card_list.html collection=home_pages %}

