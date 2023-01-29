---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: "El Balcón"
author_profile: true
header:
    overlay_image: /assets/images/balcón.jpg
show_overlay_excerpt: true
excerpt: "un punto elevado desde donde es posible, excepcionalmente, divisar un paisaje extenso <br/>  El Blog de José Martí Gómez "
entries_layout: grid
random-bestiario: true
---

{% if page.random-bestiario %}
{% include random-bestiario.html %}
{% endif %}

{% for post in site.categories.Blog limit:1 %}
<h1>{{post.title}}</h1>
{{post.content}}
{% endfor %}

