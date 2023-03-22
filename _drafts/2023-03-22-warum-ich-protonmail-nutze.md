---
layout: post
title: "Warum ich Proton Mail nutze"
categories: privacy
author:
- Florian Schuttkowski
---



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