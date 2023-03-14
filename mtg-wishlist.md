---
layout: page
title: MTG Wishlist
permalink: /mtg-wishlist/
---

{% if site.data.mtg-cards %}
Hier findest du eine regelmäßig aktualisierte Liste der Karten die ich aktuell suche. Die Tabelle ist sortiert nach Kartentyp, der Wunschpreis gibt an, welchen Preis ich für die Karte bevorzugt bezahlen möchte.  
<br />
<strong>Wichtig:</strong> Ich prüfe nicht jeden Tag die Preise jeder einzelnen Karte. Macht ihr mir also ein Angebot, prüfe ich, wieviel die Karte aktuell wert ist. Sollte sich eine größere Änderung ergeben haben, passe ich die Wunschpreise entsprechend an.

<table>
    <tr>
        <th>Karte</th>
        <th>Typ</th>
        <th>Wunschpreis</th>
    </tr>
        {% assign cards = site.data.mtg-cards | sort: "type" %}
        {% for card in cards %}
            <tr>
                <td>
                    {% if card.name %}
                        <a href="{{ card.url }}">{{ card.name }}</a>
                    {% endif %}
                </td>
                <td>{{ card.type }}</td>
                <td>{{ card.price }} €</td>
            </tr>
        {% endfor %}
</table>
{% else %}
Aktuell suche ich keine Karten. Schau gerne regelmäßig vorbei.
{% endif %}