---
layout: text 
title: Network
---

List of existing "twentyone" forks:

{% assign communities = "" | split: ',' %}

{% for country in site.data.countries %}
{% if country.offbrand %}{% continue %}{% endif %}
{% if country.link_to_public_community_group == falsy %}{% continue %}{% endif %}
{% assign communities = communities | push: country %}
{% endfor %}

{% assign names = communities | map: "name" %}
{% assign forks = names | uniq %}

<ul>
{% for name in forks %}
{% assign fork = communities | where: "name", name | first %}
<li><a href="{{ fork.link_to_public_community_group }}" target="_blank">{{ fork.name }}</a></li>
{% endfor %}
</ul>
