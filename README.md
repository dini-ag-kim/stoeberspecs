# StöberSpecs – Werkzeuge und Verfahren zur Standardisierung von Metadaten

## Die DINI AG KIM als Plattform zur Spezifikation von Metadatenstandards im Bildungsbereich

Ausgestattet mit Fördermitteln von Bund und Ländern beschäftigen sich immer mehr Akteure und Projekte im Schul- und Hochschulbereich mit dem Aufbau von Infrastrukturen zur Erstellung, Publikation und zum Teilen von Bildungsmaterialien, insbesondere [Open Educational Resources (OER)](https://de.wikipedia.org/wiki/Open_Educational_Resources). Innerhalb einer solchen Infrastruktur spielen Metadaten – strukturierte Beschreibungen, die Informationen über bestimmte Merkmale der beschriebenen Dinge erfassen – eine zentrale Rolle.

Dementsprechend stellt sich derzeit in verschiedenen Kontexten die Frage, wie OER mit Metadaten versehen werden sollten. Damit keine Parallelarbeiten stattfinden und vor allen damit die Anwendungen möglichst qualitative und homogene Metadaten aufweisen – etwa zum Zwecke der Zusammenführung und des Aufbaus übergreifender Recherchedienste – ist eine gemeinsame, fortdauernde, nachhaltige Entwicklung und Pflege von Metadatenstandards geboten.

Als ein überinstitutioneller, institutions- und projektunabhängiger Rahmen für Diskussion sowie Entwicklung und Pflege zukunftsfähiger Metadatenstandards im deutschsprachigen Raum hatte sich bereits 2013 – initiiert durch das [hbz NRW](https://www.hbz-nrw.de/) – eine [OER-Metadatengruppe](https://wiki.dnb.de/display/DINIAGKIM/OER-Metadatengruppe) innerhalb des [Kompetenzzentrums Interoperable Metadaten (KIM)](https://dini.de/ag/kim/) der [Deutschen Initiative für Netzwerkinformation (DINI)](https://dini.de/) gebildet. 2017 fusionierte diese Gruppe mit der OER-Metadatengruppe von [Jointly](https://jointly.info/). Anfang 2021 entstand aus der OER-Metadatengruppe heraus die [Curricula-Gruppe](https://wiki.dnb.de/display/DINIAGKIM/Curricula-Gruppe), deren Fokus auf der interoperablen strukturierten Beschreibung von Curricula im Bildungsbereich liegt.

Die Mailinglisten der [OER-Metadatengruppe](https://lists.dnb.de/mailman/listinfo/dini-ag-kim-oer) und der [Curricula-Gruppe](https://wiki.dnb.de/display/DINIAGKIM/Curricula-Gruppe) haben Mitglieder überwiegend aus Deutschland, aber auch aus Österreich und der Schweiz. Innerhalb der Arbeitsgruppen gibt es kontinuierlichen Austausch zu den Entwicklungen im Bereich OER-Metadaten und Curricula, monatliche Treffen finden statt. Verschiedene Spezifikationen wurden bereits publiziert, andere finden sich in Arbeit.

In Anbetracht des steigenden Interesses am Thema und der wachsenden Anzahl von Menschen, die sich damit beschäftigen, soll die Arbeitsweise der Gruppe möglichst öffentlich, transparent und partizipativ gestaltet werden. Nur so kann der Anspruch gewahrt bleiben, kontinuierlich eine zentrale Anlaufstelle für alle im deutschsprachigen Raum an OER-Metadatenstandards Interessierten zu bieten.

## Werkzeuge

Im Hinblick auf die Werkzeuge werden vorzugsweise existierende Tools benutzt, die gegebenenfalls an die spezifischen Bedingungen angepasst wurden.

### Spezifikationen, Standards, Empfehlungen

Dokumente mit offiziellem Charakter wie Spezifikationen, technische Standards und Empfehlungen werden als HTML/Markdown-Dokument verfasst und mit Hilfe eines speziellen DINI-Profils des [ReSpec](https://github.com/w3c/respec)-Präprozessors des W3C im Web publiziert. Die Quelldaten des Dokuments werden dabei auf [GitHub](https://github.com/dini-ag-kim) abgelegt, wo sie automatisch versioniert und mit einer nachvollziehbaren Änderungshistorie versehen werden. Zur Publikation kann zudem [GitHub Pages](https://pages.github.com/) verwendet werden, das lediglich in den Einstellungen des GitHub-Repositories aktiviert werden muss.

Durch die Verwendung von *ReSpec* können die Dokumente mit einer Mischung aus HTML und Markdown gepflegt werden. *ReSpec* bereitet die Dokumente automatisch für die Web-Publikation auf, indem es etwa Inhaltsverzeichnisse erstellt, Querverweise einfügt, bibliografische Referenzen nachweist und Abkürzungen auflöst. Dazu müssen lediglich einige wenige Angaben zur Konfiguration von *ReSpec* gemacht werden sowie ein paar Konventionen in der Strukturierung und dem Markup eingehalten werden. Für neue Spezifikationen sollte am besten eine bereits publizierte Spezifikation als Vorlage verwendet werden.

#### Versionierung

Für jede Spezifikation, Standard oder Empfehlung sollte ein eigenes GitHub-Repository angelegt werden. In diesem sollte sich in einem Verzeichnis `draft` die aktuelle Entwurfsfassung des Dokuments befinden, die kommentiert werden kann.

Jede publizierte Version des Dokuments sollte in einem eigenen Verzeichnis abgelegt werden, das nach der jeweiligen Versionsbezeichnung benannt ist. Es empfiehlt sich, die Versionen etwa nach ihrem Veröffentlichungsdatum zu benennen (z. B. `20200131`).

Ein symbolischer Link `latest` sollte zudem immer auf die neueste publizierte Fassung verweisen. Er dient als Referenz für Verweise auf die Spezifikation, wenn dabei nicht eine konkrete Version, sondern die jeweils gültige Fassung gemeint ist.

#### <a id="example-specs"></a>Beispiele

* **Allgemeines Metadatenprofil für Bildungsressourcen (AMB)**
    * [GitHub](https://github.com/dini-ag-kim/amb)
    * [Publikation mit ReSpec](https://w3id.org/kim/amb/latest/)
* **LOM for Higher Education OER Repositories**
    * [GitHub](https://github.com/dini-ag-kim/hs-oer-lom-profil)
    * [Publikation mit ReSpec](https://w3id.org/kim/hs-oer-lom-profil/latest/)
* **Blanko-Vorlage für neue Spezifikationen**
    * [GitHub](https://github.com/dini-ag-kim/stoeberspecs/blob/master/ReSpec/index.html)
    * [Publikation mit ReSpec](https://dini-ag-kim.github.io/stoeberspecs/ReSpec/)

### Kontrollierte Vokabulare

Auch kontrollierte Vokabulare – von einfachen Wertelisten bis zu mehrstufigen Klassifikationen – werden auf [GitHub](https://github.com/dini-ag-kim) in einem eigenen Repository abgelegt und dort versioniert und gepflegt. Als Format sollte das [Simple Knowledge Organization System (SKOS)](https://www.w3.org/2004/02/skos/) verwendet werden, wobei die Kodierung idealerweise in [Turtle](https://www.w3.org/TR/turtle/)-Syntax erfolgen sollte. Die Publikation erfolgt anschließend mit [SkoHub-Vocabs](https://github.com/skohub-io/skohub-vocabs), einer grafischen Präsentation des Vokabulars mit weitergehenden Möglichkeiten wie einer Suchfunktion (siehe [Beispiele](#example-vocab)).

#### Einführung in SKOS

Die folgende Einführung enthält auch ein Tutorial zur Erstellung und Veröffentlichung eines SKOS-Vokabulars.

* **Einführung in SKOS für den Bereich Open Educational Resources (OER)**
    * [GitHub](https://github.com/dini-ag-kim/skos-einfuehrung)
    * [Publikation](https://dini-ag-kim.github.io/skos-einfuehrung/)

#### <a id="example-vocab"></a>Beispiele

* **SKOS-Version der Destatis-Systematik der Fächergruppen, Studienbereiche und Studienfächer**
    * [GitHub](https://github.com/dini-ag-kim/hochschulfaechersystematik)
    * [Publikation mit SkoHub-Vocabs](https://w3id.org/kim/hochschulfaechersystematik/scheme)
* **Hochschulcampus Ressourcentypen (HCRT)**, eine Werteliste für Typen von Lernressourcen
    * [GitHub](https://github.com/dini-ag-kim/hcrt)
    * [Publikation mit SkoHub-Vocabs](https://w3id.org/kim/hcrt/scheme)

### Kommunikation

Zur Kommunikation wird neben gelegentlichen Präsenztreffen und monatlichen Videokonferenzen vor allem die Mailingliste der jeweiligen Gruppe verwendet. Die Listen sind öffentlich und können so von jeder/m Interessierten abonniert werden.

Die Arbeit an konkreten Spezifikationen und Standards erfolgt zusätzlich über die direkte Kommentierung der jeweiligen Entwurfsfassung (siehe oben). Diese sollte daher immer im Web publiziert werden und mit Möglichkeiten der Kommentierung versehen werden. Dazu werden die regulären GitHub-Werkzeuge wie [Issues](https://guides.github.com/features/issues/) verwendet. Kommentare in den Treffen, per Mailingliste oder [Forum](https://metadaten.community) sollen auch berücksichtigt werden.

## Organisation der Arbeitsprozesse

Vorlage für den hier beschriebenen Prozess ist der [Workflow des W3C](https://www.w3.org/2019/Process-20190301/), der jedoch aufgrund der überschaubareren Strukturen der OER-Metadatengruppe der DINI AG KIM deutlich vereinfacht wurde.

### Maintainer

Um die Pflege der Standards, Spezifikationen, Empfehlungen und Vokabulare auf GitHub zu ermöglichen, benötigt jedes Dokument mindestens eine\*n sogenannten **Maintainer\*in**. Diese Person oder Personengruppe verfügt über die notwendigen Berechtigungen, Änderungen am jeweiligen GitHub-Repository vorzunehmen. Außerdem obliegt ihr die Verantwortung, den Arbeitsprozess zu moderieren, d. h. etwa Fristen für die Kommentierung eines Entwurfs festzulegen, notwendige Abstimmungen durchzuführen oder bei Bedarf zusätzliche Kommunikationsmittel einzubeziehen (siehe oben).

Der oder die Maintainer\*innen entscheiden letztlich auch über den Zeitpunkt der Publikation einer neuen Version des betreffenden Dokuments, führen die entsprechenden strukturellen Änderungen im GitHub-Repository durch und verantworten die Endredaktion.

### Änderungsvorschläge in Pull Requests

Um die Arbeit der Maintainer\*innen so einfach wie möglich zu gestalten, sollten Änderungsvorschläge nach Möglichkeit immer in Form eines [Pull Requests](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests) auf GitHub eingereicht werden. Auf diese Weise kann der Änderungsvorschlag öffentlich kommentiert, ggf. weiter verbessert und schließlich auf Knopfdruck durch die Maintainer\*innen übernommen werden.

Wichtig ist, dass *Pull Requests* bei ReSpec immer nur Änderungen an der Entwurfsfassung im Verzeichnis `draft` beinhalten, da einmal publizierte Versionen nicht mehr substantiell geändert werden sollten. Ausnahmen stellen hier nur einfache Rechtschreibfehler oder ähnliches dar, die natürlich korrigiert werden dürfen.

Alternativ können Änderungsvorschläge natürlich auch auf herkömmlichem Weg etwa per Mailingliste an die Maintainer\*innen geschickt werden, die diese dann jedoch wiederum als *Pull Request* auf GitHub dokumentieren sollten.

### Publikation einer neuen Version mit ReSpec

Für die Publikation einer neuen Version eines mit ReSpec publizierten Dokuments sind durch die Maintainer\*innen folgende Schritte zu beachten:

1. Einen neuen Ordner anlegen und die Inhalte des Draft-Ordners da reinkopieren (als eigener Commit, um die folgenden kleinen Änderungen gegenüber dem Drat dokumentiert zu haben)
2. Den symbolischen Link aktualisieren (Linux: `ln -sfn yyyymmdd latest`, Windows: etwas kniffelig, Google hilft).
3. In der neuen Version ein paar Änderungen vornehmen:
   1. In der ReSpec-Konfig ganz am Anfang das Release-Datum aktualisieren.
   2. In der ReSpec-Konfig ganz am Anfang den Status von "unofficial" auf "base" ändern.
   3. In der ReSpec-Konfig unter "otherLinks" den Link zur neuen Version ergänzen und die Auskommentierung entfernen.
4. Falls die Spec auch vollständige Beispiele enthält, sollten die natürlich auch auf das Schema ihrer jeweiligen Version verweisen. Da müssen die Links in @schemaLocation also ggf. auch noch von "/draft/" auf das jeweilige Release geändert werden.
5. Wenn ansonsten darauf geachtet wird, dass in der Spec nur relative Links verwendet werden, muss nichts weiter angepasst werden. Eventuell noch die neue Version in der README.md ergänzen, falls irgendjemand über die GitHub-Pages-Startseite kommt.
6. Sobald die Publikation der neuen Version vollständig abgeschlossen ist, wird ein [Git Tag](https://git-scm.com/book/en/v2/Git-Basics-Tagging) für die Version vergeben sowie auf GitHub ein [Release](https://docs.github.com/en/repositories/releasing-projects-on-github/managing-releases-in-a-repository) für diese Version angelegt ([Beispiel](https://github.com/dini-ag-kim/amb/releases/tag/20231019)).

### Publikation der neuen Version eines kontrollierten Vokabulars

Bei der Aktualisierung eines bestehenden SKOS-Vokabulars sind folgende Dinge zu beachten:

1. Bereits publizierte URIs dürfen nicht gelöscht oder geändert werden.
2. Veraltete SKOS-Konzepte werden als solche mit `owl:deprecated true` markiert und – so vorhanden – mit `dct:isReplacedBy` auf das Nachfolge-Konzept verlinkt. `skos:broader`- oder `skos:narrower`-Relationen der veralteten Konzepte sollen aber unangetastet bleiben.
3. Neue Versionen werden mit einem Git tag versehen und als GitHub Releases veröffentlicht.

### Wiki

Für jedes GitHub-Repository kann in den Einstellungen ein einfaches [Wiki](https://help.github.com/en/github/building-a-strong-community/about-wikis) aktiviert werden. Dieses kann verwendet werden, um mit der Arbeit am jeweiligen Dokument in Verbindung stehende Dokumente zentral und öffentlich abzulegen (z. B. Protokolle von Videokonferenzen).
