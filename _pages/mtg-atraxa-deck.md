---
layout: page
permalink: /atraxa-deck/
title: "Mein Commander Deck: Atraxa, Praetors Voice"
---

{% assign deck = site.data.atraxa-deck %}
{% assign sorceries = site.data.atraxa-deck | where:"type","Sorcery" | sort: "drop" %}
{% assign creatures = site.data.atraxa-deck | where:"type","Creature" | sort: "drop" %}
{% assign instants = site.data.atraxa-deck | where:"type","Instant" | sort: "drop" %}
{% assign lands = site.data.atraxa-deck | where:"type","Land" | sort: "drop" %}
{% assign artifacts = site.data.atraxa-deck | where:"type","Artifact" | sort: "drop" %}
{% assign planeswalkers = site.data.atraxa-deck | where:"type","Planeswalker" | sort: "drop" %}
{% assign enchantments = site.data.atraxa-deck | where:"type","Enchantment" | sort: "drop" %}

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

## Echantments ({{enchantments.size}})
<div class="grid">
    {% for card in enchantments %}
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