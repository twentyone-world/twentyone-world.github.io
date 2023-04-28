---
layout: text 
title: List
---

{% for country in site.data.countries %}
{{ country.name }}
{% endfor %}
