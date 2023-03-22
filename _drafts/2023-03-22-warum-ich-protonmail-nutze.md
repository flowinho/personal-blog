---
layout: post
title: "Warum ich Proton Mail nutze"
categories: privacy
author:
- Florian Schuttkowski
---

**Notiz**: Dieser Artikel befasst sich explizit *nicht* mit der Frage "Warum sollte ich verschlüsselt kommunizieren?".

Privatsphäre ist ein fundamentales Recht. Dieser Satz findet sich in der Marketingmessage jedes Krypto-Software-Produkts,
von Scareware über ernstzunehmende Projekte. Und er bleibt gültig. Allerdings ist es mit der Privatsphäre im Netz einfach
immer noch nicht weit her, auch nicht im Jahre 2023. Nehmen wir mal das Beispiel Emails.

Um Emails sicher zu verschlüsseln, sollten Nutzer PGP, am besten OpenPGP mit einem auf Elliptic Curves basierten Schlüssel nutzen. Na, alles verstanden? Nein? Genau das ist das Problem. Um sinnvoll verschlüsselt zu kommunizieren, müssen Menschen 
so einiges an abstrakten Themen und Sachverhalten verstehen:

- Das Public-Key-Verfahren.
- RSA und ECC
- Passwort Manager
- Key Revocation
- Key Management, inkl. Keyserver und Revocation-Certificates
- Einbinden dieser Mechanismen in das jeweilige Betriebssystem
- Wahl von Email-Software die diese Technologien unterstützt

Wie hoch ist die Wahrscheinlichkeit, dass Menschen, die keine IT-Ausbildung haben oder kein gesteigertes Interesse in Informationstechnologie aufweisen, diese Methode aufgreifen? Ich vermute mal: nahezu Null. Die Hürden sind einfach zu groß.

Doch damit nicht genug, auch der Alltag in der Kommunikation ist oftmals ein Graus. Hier ein typischer Ablauf:

<div class="mermaid">
sequenceDiagram
    actor Sender
    actor Empfänger
    Sender-->>Empfänger: Gibt es einen Public Key?
    Empfänger-->>Sender: Ich hab da mal was auf nen KeyServer geladen.
    Sender-->>Empfänger: Ist das denn der aktuelle Key?
    Empfänger-->>Sender: Ich glaube schon, bin aber nicht sicher.
    Sender->>Empfänger: Wo finde ich deinen aktuellen Public Key?
    Empfänger->>Sender: Hier, ich schicke ihn dir.
    Sender-->>Empfänger: Danke, hier ist die Mail.
    note over Sender, Empfänger: Prozess wiederholt sich für die Rückantwort.
</div>

Darauf hat einfach niemand Lust. So etwas macht man vielleicht noch im Arbeitsumfeld mit, aber sicher nicht im privaten Umfeld. Und diese Art von Komplexität lässt sich einfach niemandem erklären. Und erst Recht nicht verargumentieren, warum diese Herangehensweise nun ständig und für jede Email ablaufen sollte.











