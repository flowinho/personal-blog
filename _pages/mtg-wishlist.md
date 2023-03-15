---
layout: page
title: MTG Wishlist
permalink: /mtg-wishlist/
---

{% if site.data.mtg-cards %}
Hier findest du eine regelmäßig aktualisierte Liste der Karten die ich aktuell suche. Die Tabelle ist sortiert nach Kartentyp, der Wunschpreis gibt an, welchen Preis ich für die Karte bevorzugt bezahlen möchte.  
<br />
<strong>Wichtig:</strong> Ich prüfe nicht jeden Tag die Preise jeder einzelnen Karte. Macht ihr mir also ein Angebot, prüfe ich, wieviel die Karte aktuell wert ist. Sollte sich eine größere Änderung ergeben haben, passe ich die Wunschpreise entsprechend an. Sollte kein Preis angezeigt werden, habe ich die Karte meiner Wishlist hinzugefügt, aber noch nicht nach einem akzeptablen Preis gesucht.

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
                        {% if card.url %}
                            <a href="{{ card.url }}">{{ card.name }}</a>
                        {% else %}
                            {{ card.name }}
                        {% endif %}
                    {% endif %}
                </td>
                <td>
                    {% if card.type %}
                        {{ card.type }}
                    {% endif %}
                </td>
                <td>
                    {% if card.price %}
                        {{ card.price }} €
                    {% endif %}
                </td>
            </tr>
        {% endfor %}
</table>
{% else %}
Aktuell suche ich keine Karten. Schau gerne regelmäßig vorbei.
{% endif %}