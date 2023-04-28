---
layout: text 
title: Network
---

[twentyone.world](/) is a network of open communities that provide localized,
high-quality, [bitcoin-only](/focus) content. Each community provides an [open
space](/space) for bitcoiners in their respective countries to connect,
collaborate, and exchange ideas. Each community has a [beacon](/beacon) in
cyberspace that speaks the [language](/language) of their respective community.

The purpose of [twentyone.world](/) is to open-source the concept, provide an
actionable [blueprint](/blueprint) to help bitcoiners launch their own
communities, and connect said communities to learn from each other.

## Communities

List of existing "twentyone" forks:

{% assign communities = "" | split: ',' %}

{% for country in site.data.countries %}
{% if country.offbrand %}{% continue %}{% endif %}
{% if country.link_to_public_community_group == falsy %}{% continue %}{% endif %}
{% assign communities = communities | push: country %}
{% endfor %}

{% assign names = communities | map: "name" %}
{% assign forks = names | uniq %}

{% for name in forks %}
{% assign fork = communities | where: "name", name | first %}
- [{{ fork.name }}]({{ fork.link_to_public_community_group }})
{% endfor %}

[← Back to the map](/)

---
