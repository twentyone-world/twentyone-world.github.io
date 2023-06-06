---
layout: text 
title: Network
---

The "network" part is very much a work-in-progress. If you've started a fork
and/or would like to help, please [contact me](https://dergigi.com/contact).

If you want to hang out with like-minded people and understand more about the
concept, feel free to join the open group of twentyone.world:

<center>
    <a href="https://t.me/twentyonedotworld" target="_blank">
        <button type="button" class="btn btn-primary btn-large btn-custom">Join the Group</button>
    </a>
</center>

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