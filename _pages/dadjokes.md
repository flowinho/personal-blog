---
layout: page
title: Dad Jokes
permalink: /dadjokes/
---

Die Witze auf dieser Website sind nicht zwingend Dad Jokes, also nicht immer Wortwitze. Meistens aber. Wo möglich, und falls dafür Zeit ist, verlinke ich die Quelle des Witzes.

<ul>
{% assign jokes = site.data.dadjokes %}
{% for joke in jokes %}
    <li>
        {{ joke.text }}
        {% if joke. src %}
            <br />
            <span class="dadjoke-src">Quelle: {{ joke.src }}</span>
        {% endif %}
    </li>
{% endfor %}
</ul>