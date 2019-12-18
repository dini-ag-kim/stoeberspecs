## Format

Eine Visitenkarte wird durch ein JSON-Objekt repräsentiert. Dieses JSON-Objekt beinhaltet obligatorische wie optionale Schlüssel/Werte-Paare.

Neben allgemeinen Informationen zur Applikation werden auch die speziellen Services mitgeteilt, die extern nutzbar sind (Suche, Harvesting, Tools).

Die Visitenkarte einer Applikation wird im JSON-LD-Format bereitgestellt, entweder als eigenes JSON-Dokument oder eingebettet in die Startseite. Die URL, hinter der sich das Dokument befindet, kann dann abgefragt und die resultierenden Inhalte ausgewertet werden.

Wird die Visitenkarte als JSON-Dokument angeboten, sollte der folgende `Content-Type` Header gesetzt werden:

```
    Content-Type: application/ld+json
```

Wenn das JSON-Dokument in die Startseite der Applikation eingebettet wird, geschieht dies mit Nutzung eines `script`-Tags vornehmlich im `head`-Bereich:

```
    <script type="application/ld+json">
        [...]
    </script>
```

Alternativ kann eine Discovery-URL in die Seite eingebunden werden:

```
    <link rel="meta" type="application/ld+json" href="[...]" title="Service-Description" />
```

Oder mittels `Link`-Header und Relation `meta` kommuniziert werden:

```
    HTTP/1.1 200 OK
    Link: <[...]>; rel="meta"
```
