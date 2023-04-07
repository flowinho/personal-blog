---
layout: post
title: "Tipp: Breite für einzelne Bilder in Jekyll definieren"
categories: jekyll
author:
- Florian Schuttkowski
---

Ein sehr kurzer Post, mit dem ich eine kleine aber wichtige Erkenntnis dokumentieren möchte: Jekyll unterstützt eine Notation, mit die Größe von Bilder direkt definiert werden kann. Gefunden habe ich diese Notation in dem zuerst unscheinbar anmutenden Kommentar von Rohit Tahiliani zu [diesem Blogpost](https://dev-notes.eu/2016/01/images-in-kramdown-jekyll/).

Mit der mir bisher bekannten Syntax zur Inkludierung von Bilder in Markdown war ich recht zufrieden. Doch mit Hilfe dieser zusätzlichen Syntax lassen sich Bilder um einiges leichter positionieren und definieren und der gesammte Prozess des Schreibens erweitert sich um eine mir bisher unbekannte Flexibilität.

```markdown
// Standard
![](bild.jpg)

// Ein Bild mit alternativem Text. Sollte immer gemacht werden!
// Bitte denkt an Accessability.
![ein bild](bild.jpg)   

// Ein Bild mit "spontan" gesetzter fester Breite.
![ein bild](bild.jgg){:width="333px"}

// Ein Bild mit "spontan" gesetzter, prozentualer Höhe.
![ein bild](bild.jgg){:height="33%"}
```

**Wichtig:** Es gibt verschiedene Syntax für diese Definitionen. `{:width="<value>"` funktioniert für das von Jekyll standardmäßig verwendete Kramdown. Für andere Markdown-Interpreter gilt womöglich eine alternative Schreibweise.