---
layout: post
title: "Zitat des Tages: Wir committen wenn wir fertig sind"
categories: slice-of-life
author:
- Florian Schuttkowski
---

In einem Planning-Meeting heute stellte ich die Frage: "Wo liegt denn der aktuelle Code? Kann ich den mal sehen?". Es ist mir als Architekt wichtig, dass wir kurze Feedback-Loops in unserem Team etablieren. Nicht umsonst freue ich mich über unsere Entscheidung, [trunk based development](https://trunkbaseddevelopment.com/) einzuführen. Schließlich profitiert das gesamte Team davon, wenn alle Entwickler:innen bereits früh zumindest mitbekommen _können_, in welche Richtung sich die Codebase eines Projekt bewegt. 

> "Der Code liegt noch in einem privaten Repository, ich pushe ihn auf den zentralen SCM-Server, wenn er perfekt ist und ich fertig bin." -- Kolleg:in

Mal abgesehen davon, dass Code zu keinem Zeitpunkt perfekt ist oder sein kann, habe ich mit dieser Aussage so meine Probleme:

1. **Software Entwicklung ist ein Teamgame**  
Alleine zu programmieren hat Vorteile. Man hat seine Ruhe, kann Entscheidungen selbt treffen und behält die Hoheit über den Code. Nicht ohne Grund erfreuen sich Feature-Branches, die Personen zugeordnet sind, immer noch großer Beliebtheit. "My code is my castle." Hier pfuscht mir keiner rein. Doch die Nachteile sind gravierend, sofern der:die Entwickler:in in einem Team arbeitet. Nachträgliche Anmerkungen, möglicherweise falsch getroffene Entscheidung und daraus resultierende Reworks und ein dedizierter Aufschlauen der Kolleg:innen sind mögliche Folge eines solchen Alleingangs. 
2. **Mögliche Anforderungen werden unbewusst nicht implementiert**  
Hat niemand Einsicht in den Quellcode, können auch assistierende technische Rollen wie ein Architekt oder ein technischer Product Owner keinen Blick in den laufenden Entwicklungsstand werfen. Auch andere Kolleg:innen, die über weiterführende Informationen verfügen, können keinen Beitrag leisten. Somit erzeugt die Entscheidung für eine isolierte Codebase für Fehlerpotential und mögliche Unvollständigkeit.
3. **Potentielles Risiko des Verlusts von Code**  
Wer ein Backup hat, hat kein Backup. Wer zwei Backups hat, hat ein Backup. Aber wer seinen Code auf einem zentralen Server hat, hat immer die Möglichkeit den potentiellen Verlust eines Entwicklungsgeräts wieder auszugleichen und den Code erneut von dort zu beziehen.
    - Im Corporate Environment besteht die Gefahr, dass IP der Firma abhanden oder gar bei der Konkurrenz ankommt, sollten Entwickler:innen ihre Geräte nicht entsprechend sichern.
    - Trotz allgemeinem Vertrauens besteht die Möglichkeit, dass sowohl Freiberufler als auch Angestellte sich durch die Kontrolle über den Sourcecode entweder unersetzbar machen oder bereits in LOC investiertes Geld unter Verschluss gehalten wird.
4. **Niemand lernt etwas**  
Niemand sitzt gerade in Workshops oder PowerPoint-Präsentationen. Durch das Teilen von Code und Peer Reviews werden die Kollegen quasi on-the-fly aufgeschlaut und über den aktuellen Stand sowie neue technologische Implementierungen informiert und aufgeschlaut. Liegt der Code einzig bei einer Person, muss diese Person das gesamte Team auf den aktuellen Stand bringen. Ein unnötiger Aufwand.
5. **Entwickler:in ist alleine für die Qualität zuständig**  
Da niemand Zugriff auf den Code hat, trägt die ihn implementierende oder wartende Person die alleinge Verantwortung.

Zusammenfassend kann mal also die fundierte Behauptung aufstellen, dass ein Alleingang in der Softwareentwlickung trotz Zugehörigkeit zu einem Team als geschäftsschädigendes Verhalten gewertet kann. Bitte seid nicht diese Person.

Hier das Ganze nochmal als Schaubild 😎 Mit Notes!

<div class="mermaid">
stateDiagram
[*] --> SCMServer
SCMServer --> Review

    note right of Review
    Hier lernen alle etwas!
    end note

Review --> PRRemark
PRRemark --> SCMServer
Review --> CleanCode
CleanCode --> [*]

SCMServer --> NoReview

    note left of NoReview
    Hier lernt niemand etwas!
    end note

NoReview --> BadCode

    note right of BadCode
    Höchst wahrscheinlich grottiger Code.
    end note

BadCode --> [*]

</div>