---
layout: page
title: Дисциплины
permalink: /courses/
---

{% for sem in (1..6) %}
### {{ sem | plus: 1 | divided_by: 2 }} курс, {{ sem }} семестр
<!-- Source: https://github.com/abhinavs/moonwalk -->
  {% assign courses = site.courses | where: "semester", sem %}
  {% include course_list.html collection=courses %}
{% endfor %}

