---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: Системное программирование ММФ НГУ
---

## Наши курсы

{% for sem in (1..6) %}
### {{ sem | plus: 1 | divided_by: 2 }} курс, {{ sem }} семестр
<!-- Source: https://github.com/abhinavs/moonwalk -->
  {% assign courses = site.courses | where: "semester", sem %}
  {% include course_list.html collection=courses %}
{% endfor %}

