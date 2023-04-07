---
layout: page
permalink: /atraxa-deck/
title: "Mein Commander Deck: Atraxa, Praetors Voice"
---

{% assign deck = site.data.atraxa-deck %}
{% assign sorceries = site.data.atraxa-deck | where:"type","Sorcery" %}
{% assign creatures = site.data.atraxa-deck | where:"type","Creature" %}
{% assign instants = site.data.atraxa-deck | where:"type","Instant" %}
{% assign lands = site.data.atraxa-deck | where:"type","Land" %}
{% assign artifacts = site.data.atraxa-deck | where:"type","Artifact" %}
{% assign planeswalkers = site.data.atraxa-deck | where:"type","Planeswalker" %}

## Creatures ({{creatures.size}})
<div class="grid">
    {% for card in creatures %}
        {% include card.html card=card %}
    {% endfor %}
</div>

## Sorceries ({{sorceries.size}})
<div class="grid">
    {% for card in sorceries %}
        {% include card.html card=card %}
    {% endfor %}
</div>

## Instants ({{instants.size}})
<div class="grid">
    {% for card in instants %}
        {% include card.html card=card %}
    {% endfor %}
</div>

## Artifacts ({{artifacts.size}})
<div class="grid">
    {% for card in artifacts %}
        {% include card.html card=card %}
    {% endfor %}
</div>

## Planeswalker ({{planeswalkers.size}})
<div class="grid">
    {% for card in planeswalkers %}
        {% include card.html card=card %}
    {% endfor %}
</div>

## Lands ({{lands.size}})
<div class="grid">
    {% for card in lands %}
        {% include card.html card=card %}
    {% endfor %}
</div>