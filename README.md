# OER-StöberSpecs

Werkzeuge und Verfahren zur Standardisierung von OER-Metadaten

## AP1: Evaluation von Spec Präprozessoren

### <a id="respec"></a>[ReSpec](https://github.com/w3c/respec)

* [OER Service Card](https://github.com/dini-ag-kim/oer-service-card/) (multi-file spec)
  * Publizierte Version: https://dini-ag-kim.github.io/oer-service-card/
* [HS-OER LOM-Profil](https://github.com/dini-ag-kim/hs-oer-lom-profil/) (single-file spec)
  * Publizierte Version: https://dini-ag-kim.github.io/hs-oer-lom-profil/

##### Vorteile

- keine statische Generierung von HTML-Seiten ([bei Bedarf aber möglich](https://github.com/w3c/respec/wiki/ReSpec-Editor's-Guide#creating-a-static-snapshot))
- unterstützt Strukturierung in mehreren Dateien
- für die Publikation von technischen Spezifikationen entwickelt
- automatische Generierung/Auszeichnung von
  - Inhaltsverzeichnis
  - Glossar/Abkürzungen
  - Referenzlisten und Literaturangaben
  - Querverweisen
- leicht zu lernen: HTML und Markdown

##### Nachteile

- W3C-spezifisches Rendering nur durch eigenes [Profil](https://github.com/w3c/respec/wiki/Developers-Guide#custom-profiles) änderbar
- [Multilingualität](https://github.com/w3c/respec/blob/develop/src/core/l10n.js) wird unterstützt
  - Deutsche Übersetzung hinzugefügt: https://github.com/w3c/respec/pull/2687 & https://github.com/w3c/respec/pull/2710

## AP2: Prozess zur Spezifikation eines Metadatenschemas

- Standardisierungsprozess findet öffentlich auf GitHub statt, um jedem Interessierten die Teilnahme zu ermöglichen
- es gibt jeweils eine aktuelle Arbeitsversion (draft), die kommentiert werden kann (per GitHub und [hypothes.is](https://web.hypothes.is/))
- jede Spezifikation wird in einem eigenen Repository gepflegt
- publizierte Versionen werden in eigene Verzeichnisse im Repo verschoben, um via GitHub Pages versionsspezifische URIs zu erhalten
  - Namenskonvention: Verzeichnisname ist Veröffentlichungsdatum der Version
  - Vorschlag für Verzeichnisstruktur:
    - `README.md` (als Einstiegspunkt für GitHub Pages)
    - `draft/` (aktuelle Arbeitsversion zur Kommentierung)
    - `20190309/` (Version vom 09.03.2019)
    - `20200116/` (Version vom 16.01.2020)
    - [...]
    - `latest/` (symbolischer Link auf jeweils aktuellste Version)
- Aktualisierungen der Arbeitsversion erfolgen über Pull-Requests
  - durch die Strukturierung in einzelne Dateien können verschiedene Gruppen/Personen leichter ohne Editier-Konflikte gleichzeitig an unterschiedlichen Bereichen der Spezifikation arbeiten
  - Strukturierung in einzelne Dateien geht jedoch zu Lasten der Performance beim Rendering der Spezifikation
    - optional könnten daher bei Release einer neuen Version alle Inhalte in ein zentrales Dokument übernommen werden
    - alternativ kann auch ein [statischer Snapshot](https://github.com/w3c/respec/wiki/ReSpec-Editor's-Guide#creating-a-static-snapshot) publiziert werden, dann wäre die Spezifikation auch ohne Javascript nutzbar
- es braucht mindestens eine Person in der Rolle des Maintainers, d. h. mit erweiterten Rechten für das GitHub-Repository
  - Maintainer moderiert den Kommentierungsprozess, pflegt Änderungen ein und veröffentlicht neue Versionen der Spezifikation
  - Maintainer kann auch eine Gruppe von Personen sein
- Werkzeuge der Arbeitsgruppe sind
  - GitHub-Repository (als zentrales Arbeits- und Versionierungswerkzeug)
    - über Issues und Pull-Request kann auch Kommunikation/Diskussion sowie aktive Mitarbeit abgebildet werden
  - GitHub Pages (für die automatische Publikation von Drafts und finaler Spezifikation)
  - GitHub Wiki (als Ablage für Protokolle, Entscheidungsvorlagen, weitergehende Dokumentation, etc.)
  - Mailingliste (als niedrigschwelliges und allgemeines Kommunikationsmittel)
  - [hypothes.is](https://web.hypothes.is/) (als niedrigschwellige Annotationsmöglichkeit an Drafts)

## AP4: Einführung in SKOS

* [Erste Überlegungen in CodiMD-Pad](https://pad.gwdg.de/D-QEi-z6RleT1kxBccpWww)
