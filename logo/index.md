---
layout: text 
title: Fork the Logo
---

To keep it simple: "twentyone", translated to your local language, [bold font], with a small [bitcoin logo].

Like this, but not in English:

![](/logo/paths/twentyone.svg)

Some forks also use a square or multi-line style:

![](/logo/paths/twe-nty-one.svg)
![](/logo/paths/twenty-one.svg)

## Download Template & Font

* All of it: [everything.zip][everything]
* SVG templates: [horizontal](/logo/twentyone.svg), [square](/logo/twe-nty-one.svg), [two lines](/logo/twenty-one.svg)
* Font: [The Bold Font][bold font][^bold]


You can use [Inkscape][inkscape][^inkscape] to modify the SVG files to your needs.

[^bold]: Free font by New Bold Times, [dafont.com](https://www.dafont.com/the-bold-font.font)
[^inkscape]: Inkscape is free, libre, open-source software, [inkscape.org][inkscape]

## Existing Forks

Make sure to have [The Bold Font][bold font] installed, or some of the below might render weird.

{% for image in site.static_files %}
{% if image.path contains 'logo/forks' %}
![]({{ image.path }})
{% endif %}
{% endfor %}

Did you create a fork and your logo isn't listed above? Add your logo to [this folder](https://github.com/twentyone-world/twentyone-world.github.io/tree/main/logo/forks) to make it appear above! 


[inkscape]: https://inkscape.org/
[bold font]: {{ '/logo/the_bold_font.zip' | absolute_url }}
[bitcoin logo]: {{ '/logo/bitcoin.svg' | absolute_url }}
[everything]: {{ '/logo/everything.zip' | absolute_url }}
