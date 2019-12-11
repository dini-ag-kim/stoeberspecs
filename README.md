# OER-StöberSpecs

Werkzeuge und Verfahren zur Standardisierung von OER-Metadaten

## AP1: Evaluation von Spec Präprozessoren

### <a id="respec"></a>[ReSpec](https://github.com/w3c/respec)

* [ReSpec Demo](evaluation/ReSpec/demo-unofficial.html) (Status: "unofficial")
* [ReSpec Demo](evaluation/ReSpec/demo-base.html) (Status: "base")

##### Vorteile

- keine statische Generierung von HTML-Seiten
- für die Publikation von technischen Spezifikationen entwickelt
- leicht zu lernen: HTML

##### Nachteile

- W3C-spezifisches Rendering nur durch eigenen Fork änderbar
- ungewisse Perspektive: W3C migriert von ReSpec zu [Bikeshed](#bikeshed)

### <a id="bikeshed"></a>[Bikeshed](https://github.com/tabatkins/bikeshed)

* [Bikeshed Demo](https://tabatkins.github.io/bikeshed/) (externer Link)

##### Vorteile

- für die Publikation von technischen Schnittstellen entwickelt
- leicht zu lernen: Markdown

##### Nachteile

- W3C-spezifisches Rendering nur durch eigenen Fork änderbar
- kein on-the-fly Rendering der Spezifikation möglich (aber Travis CI Integration in GitHub)

### <a id="docsify"></a>[docsify](https://github.com/docsifyjs/docsify)

* [docsify Demo](evaluation/docsify/index.html)

##### Vorteile

- keine statische Generierung von HTML-Seiten
- unterstützt Strukturierung in mehreren Dateien
- integrierte Volltextsuche
- über [Plugins](https://docsify.js.org/#/plugins) erweiterbar
- leicht zu lernen: Markdown

##### Nachteile

- keine spezifische Funktionalität für technische Spezifikationen

## AP4: Einführung in SKOS

* [Erste Überlegungen in CodiMD-Pad](https://pad.gwdg.de/D-QEi-z6RleT1kxBccpWww)
