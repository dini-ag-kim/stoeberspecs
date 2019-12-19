# OER-StöberSpecs

Werkzeuge und Verfahren zur Standardisierung von OER-Metadaten

## AP1: Evaluation von Spec Präprozessoren

### <a id="respec"></a>[ReSpec](https://github.com/w3c/respec) (<- Empfehlung)

* [ReSpec Demo](evaluation/ReSpec/demo-service-card.html) (OER Service Card)

##### Vorteile

- keine statische Generierung von HTML-Seiten
- unterstützt Strukturierung in mehreren Dateien
- für die Publikation von technischen Spezifikationen entwickelt
- automatische Generierung/Auszeichnung von
  - Inhaltsverzeichnis
  - Glossar/Abkürzungen
  - Referenzlisten und Literaturangaben
- leicht zu lernen: HTML und Markdown

##### Nachteile

- W3C-spezifisches Rendering nur durch eigenes [Profil](https://github.com/w3c/respec/wiki/Developers-Guide#respecs-architecture) änderbar
- [Multilingualität](https://github.com/w3c/respec/blob/develop/src/core/l10n.js) wird grundsätzlich unterstützt, aber derzeit keine deutsche Übersetzung

### <a id="bikeshed"></a>[Bikeshed](https://github.com/tabatkins/bikeshed)

* [Bikeshed Dokumentation](https://tabatkins.github.io/bikeshed/) (mit Bikeshed erstellt)

##### Vorteile

- weitgehend identisches Feature-Set wie [ReSpec](#respec)

##### Nachteile

- kein on-the-fly Rendering der Spezifikation durch Einbinden eines Javascripts möglich, erfordert Prozesskette (z. B. mit [Travis CI](https://tabatkins.github.io/bikeshed/#travis-ci))

### <a id="docsify"></a>[docsify](https://github.com/docsifyjs/docsify)

* [docsify Dokumentation](https://docsify.js.org/#/) (mit docsify erstellt)
* [docsify Showcase](https://github.com/docsifyjs/awesome-docsify#showcase) (weitere Anwendungsbeispiele)

##### Vorteile

- keine statische Generierung von HTML-Seiten
- unterstützt Strukturierung in mehreren Dateien
- integrierte Volltextsuche
- über [Plugins](https://docsify.js.org/#/plugins) erweiterbar
- leicht zu lernen: Markdown

##### Nachteile

- keine spezifische Funktionalität für technische Spezifikationen

## AP2: Prozess zur Spezifikation eines Metadatenschemas

- Standardisierungsprozess findet öffentlich auf GitHub statt, um jedem Interessierten die Teilnahme zu ermöglichen
- es gibt jeweils eine aktuelle Arbeitsversion (draft), die über eine [hypothes.is](https://web.hypothes.is/)-Einbindung niedrigschwellig kommentiert werden kann
  - Kommentierung kann auch über den GitHub-Workflow (Zeilen- und Blockkommentare, Issues, Pull-Requests) erfolgen
    - weniger niedrigschwellig, dafür weniger Arbeit für Maintainer
- publizierte Versionen werden in eigene Verzeichnisse im Repo verschoben, um via GitHub Pages versionsspezifische URIs zu erhalten
  - Vorschlag für Verzeichnisstruktur:
    - README.md (als Einstiegspunkt für GitHub Pages)
      - [Name der Spezifikation] (z. B. `service-card`)
        - `draft` (aktuelle Arbeitsversion zur Kommentierung)
        - `v1` (erste publizierte Version, ggf. auch [semantische Versionierung](https://semver.org/))
        - `v2` (zweite publizierte Version)
        - [...]
        - `latest` (symbolischer Link auf jeweils aktuellste Version)
- Aktualisierungen der Arbeitsversion erfolgen über Pull-Requests
  - durch die Strukturierung in einzelne Dateien können verschiedene Gruppen/Personen leichter ohne Editier-Konflikte gleichzeitig an unterschiedlichen Bereichen der Spezifikation arbeiten
  - Strukturierung in einzelne Dateien geht jedoch zu Lasten der Performance beim Rendering der Spezifikation
    - optional könnten daher bei Release einer neuen Version alle Inhalte in ein zentrales Dokument übernommen werden
- es braucht mindestens eine Person in der Rolle des Maintainers, d. h. mit erweiterten Rechten für das GitHub-Repository
  - Maintainer moderiert den Kommentierungsprozess, pflegt Änderungen ein und veröffentlicht neue Versionen der Spezifikation

## AP4: Einführung in SKOS

* [Erste Überlegungen in CodiMD-Pad](https://pad.gwdg.de/D-QEi-z6RleT1kxBccpWww)
