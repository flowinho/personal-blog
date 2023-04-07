---
layout: page
permalink: /atraxa-deck/
title: "Mein Commander Deck: Atraxa, Praetors Voice"
---

<style>
.grid { 
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(272px, 1fr));
  grid-gap: 16px;
  align-items: stretch;
  }
.grid > card {
  border: 1px solid #ccc;
  border-radius: 6px;
}
.grid > card img {
  max-width: 100%;
  margin-top: 16px;
}
.text {
  margin-top: 16px;
  margin-left: 8px;
  margin-right: 16px;
}
.card-title {
    font-weight: bold;
}
.card-type {
    color: darkgray;
    border-bottom: 1px solid #ccc;
}
</style>

## Statistics

{% assign deck = site.data.atraxa-deck %}
{% assign sorceries = site.data.atraxa-deck | where:"type","Sorcery" %}

## Sorceries
<!-- {% assign deck = site.data.atraxa-deck | where:"type","Sorcery" %} -->
{% assign deck = site.data.atraxa-deck %}
<div class="grid">
    {% for card in deck %}
    <card>
        <div class="card-type" align="center">
            {{ card.type }}
        </div>
        <div align="center">
            <img src="{{ card. image }}" />
        </div>
        <div class="text">
            <div align="center">
                <span class="card-title">{{ card.name }}</span>
            </div>
            <ul>
            {% for reason in card.reasons %}
                <li>{{ reason }}</li>
            {% endfor %}
            </ul>
        </div>
    </card>
    {% endfor %}
</div>