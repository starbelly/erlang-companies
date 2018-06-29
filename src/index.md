---
layout: default
---
{% assign cards = site.data[site.cards.data] %}
{% include hero-intro.html %}
{% include section-cards.html caption=page.title cards=cards %}
