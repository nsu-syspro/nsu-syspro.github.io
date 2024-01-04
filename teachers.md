---
layout: page
title: Преподаватели
permalink: /teachers/
---

{% assign teachers = site.teachers | sort: "name" %}
{% include teacher_list.html collection=teachers show_courses=true %}
