## Vocabulary

The normative vocabulary for service cards is [[schema.org]]. The complete sub-set of properties used for service cards is described in this section.

For each property a short description, the degree if obligation (`mandatory`, `optional`), the data type and - if applicable - the range of allowed values is given.

<section data-dfn-for="@context">

### <dfn>@context</dfn>

This holds the JSON-LD context as a reference.

<dl>
    <dt>Obligation</dt>
    <dd>mandatory</dd>
    <dt>Data Type</dt>
    <dd>URL</dd>
    <dt>Values</dt>
    <dd>`https://schema.org/`</dd>
</dl>

</section>

<section data-dfn-for="id">
    <h2><dfn>id</dfn></h2>
    <p>
        Die URL, durch die der Service identifiziert wird. Das ist in der Regel die Homepage. Auf dieser URL MUSS die Visitenkarte später abrufbar sein
    </p>
    <dl>
        <dt>Pflichtangabe</dt>
        <dd>ja</dd>
    </dl>
    <dl>
        <dt>Datentyp</dt>
        <dd>URL</dd>
    </dl>
</section>
<section data-dfn-for="type">
    <h2><dfn>type</dfn></h2>
    <p>
        Art der Webseite
    </p>
    <dl>
        <dt>Pflichtangabe</dt>
        <dd>ja</dd>
    </dl>
    <dl>
        <dt>Datentyp</dt>
        <dd>URL</dd>
    </dl>
    <dl>
        <dt>Wertebereich</dt>
        <dd>`https://schema.org/WebSite` und `https://schema.org/Service`</dd>
    </dl>
</section>
<section data-dfn-for="name">
    <h2><dfn>name</dfn></h2>
    <p>
        Name des Dienstes
    </p>
    <dl>
        <dt>Pflichtangabe</dt>
        <dd>ja</dd>
    </dl>
    <dl>
        <dt>Datentyp</dt>
        <dd>`String`</dd>
    </dl>
</section>
<section data-dfn-for="image">
    <h2><dfn>image</dfn></h2>
    <p>
        Icon des Dienstes. Kann genutzt werden, um beispielsweise Suchergebnisse zu kennzeichnen
    </p>
    <dl>
        <dt>Pflichtangabe</dt>
        <dd>nein</dd>
    </dl>
    <dl>
        <dt>Datentyp</dt>
        <dd>URL</dd>
    </dl>
    <dl>
        <dt>Wertebereich</dt>
        <dd>Dateiformat: `svg`, `png` (64x64px)</dd>
    </dl>
</section>
<section data-dfn-for="logo">
    <h2><dfn>logo</dfn></h2>
    <p>
        Logo des Dienstes
    </p>
    <dl>
        <dt>Pflichtangabe</dt>
        <dd>nein</dd>
    </dl>
    <dl>
        <dt>Datentyp</dt>
        <dd>URL</dd>
    </dl>
</section>
<section data-dfn-for="inLanguage">
    <h2><dfn>inLanguage</dfn></h2>
    <p>
        Sprache(n) des Hauptangebotes
    </p>
    <dl>
        <dt>Pflichtangabe</dt>
        <dd>nein</dd>
    </dl>
    <dl>
        <dt>Datentyp</dt>
        <dd>`String[]`</dd>
    </dl>
    <dl>
        <dt>Wertebereich</dt>
        <dd>[[IETFBCP47]]</dd>
    </dl>
</section>
<section data-dfn-for="description">
    <h2><dfn>description</dfn></h2>
    <p>
        Beschreibung des Dienstes
    </p>
    <dl>
        <dt>Pflichtangabe</dt>
        <dd>nein</dd>
    </dl>
    <dl>
        <dt>Datentyp</dt>
        <dd>`String`</dd>
    </dl>
</section>
<section data-dfn-for="serviceType">
    <h2><dfn>serviceType</dfn></h2>
    <p>
        Art des Services
    </p>
    <dl>
        <dt>Pflichtangabe</dt>
        <dd>ja</dd>
    </dl>
    <dl>
        <dt>Datentyp</dt>
        <dd>`String[]`</dd>
    </dl>
    <dl>
        <dt>Wertebereich</dt>
        <dd>`Repository`, `Referatory`, `Wiki`, `LMS`</dd>
    </dl>
</section>
<section>
    <h2>[...]</h2>
</section>
