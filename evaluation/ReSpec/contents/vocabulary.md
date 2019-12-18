## Vocabulary

The normative vocabulary for service cards is [[schema.org]]. The complete sub-set of properties used for service cards is described in this section.

For each property a short description, the degree if obligation (`mandatory`, `optional`), the data type and - if applicable - the range of allowed values is given. For reference the [[schema.org]] definition is given as well.

<section data-dfn-for="@context">

### <dfn>@context</dfn>

This holds the JSON-LD context as a reference. This MUST be `https://schema.org/`. Thus all properties of the service card can be prepended with `https://schema.org/` to get their full URI.

<dl>
    <dt>Obligation</dt>
    <dd>mandatory</dd>
    <dt>Data Type</dt>
    <dd>URI</dd>
    <dt>Values</dt>
    <dd>`https://schema.org/`</dd>
</dl>

</section>

<section data-dfn-for="id">

### <dfn>id</dfn>

An URL identifying the service described by the service card. The service card MUST be published at this URL.

<dl>
    <dt>Obligation</dt>
    <dd>mandatory</dd>
    <dt>Data Type</dt>
    <dd>URL</dd>
    <dt>[[schema.org]] definition</dt>
    <dd>http://schema.org/id</dd>
</dl>

</section>

<section data-dfn-for="type">

### <dfn>type</dfn>

<p class="note" title="[[schema.org]] definition">
    http://schema.org/type
</p>

The type of the application described by the service card. This MUST be `https://schema.org/WebSite` and `https://schema.org/Service`.

<dl>
    <dt>Obligation</dt>
    <dd>mandatory</dd>
    <dt>Data Type</dt>
    <dd>URL</dd>
    <dt>Values</dt>
    <dd>`https://schema.org/WebSite` and `https://schema.org/Service`</dd>
</dl>

</section>

<section data-dfn-for="name">

### <dfn>name</dfn>

<p class="note" title="[[schema.org]] definition">
    http://schema.org/name
</p>

The name of the application or service described by the service card.

<dl>
    <dt>Obligation</dt>
    <dd>mandatory</dd>
    <dt>Data Type</dt>
    <dd>`String`</dd>
</dl>

</section>

<section data-dfn-for="image">

### <dfn>image</dfn>

<p class="note" title="[[schema.org]] definition">
    http://schema.org/image
</p>

An icon for the service. This MAY be used by third-party applications implementing the service.

<dl>
    <dt>Obligation</dt>
    <dd>optional</dd>
    <dt>Data Type</dt>
    <dd>URL</dd>
    <dt>Values</dt>
    <dd>Format: `svg` or `png`<br>Size: 64x64px</dd>
</dl>

</section>

<section data-dfn-for="logo">

### <dfn>logo</dfn>

<p class="note" title="[[schema.org]] definition">
    http://schema.org/logo
</p>

A logo for the application or service. This MAY also be the logo of the hosting institution or other provider.

<dl>
    <dt>Obligation</dt>
    <dd>optional</dd>
    <dt>Data Type</dt>
    <dd>URL</dd>
</dl>

</section>

<section data-dfn-for="inLanguage">

### <dfn>inLanguage</dfn>

<p class="note" title="[[schema.org]] definition">
    http://schema.org/inLanguage
</p>

The primary language(s) of the content provided by the service. If given, this MUST be one or more of [[IETFBCP47]].

<dl>
    <dt>Obligation</dt>
    <dd>optional</dd>
    <dt>Data Type</dt>
    <dd>`String[]`</dd>
    <dt>Values</dt>
    <dd>[[IETFBCP47]]</dd>
</dl>

</section>

<section data-dfn-for="description">

### <dfn>description</dfn>

<p class="note" title="[[schema.org]] definition">
    http://schema.org/description
</p>

A short description of the application or service.

<dl>
    <dt>Obligation</dt>
    <dd>optional</dd>
    <dt>Data Type</dt>
    <dd>`String` (`http://schema.org/description`)</dd>
</dl>

</section>

<section data-dfn-for="serviceType">

### <dfn>serviceType</dfn> (`http://schema.org/serviceType`)

<p class="note" title="[[schema.org]] definition">
    http://schema.org/serviceType
</p>

The type(s) of service provided by the application. This MAY be one or more of `Repository`, `Referatory`, `Wiki`, `LMS`.

<dl>
    <dt>Obligation</dt>
    <dd>mandatory</dd>
    <dt>Data Type</dt>
    <dd>`String[]`</dd>
    <dt>Values</dt>
    <dd>`Repository`, `Referatory`, `Wiki`, `LMS` or any other</dd>
</dl>

</section>

<section>
    <h2>[...]</h2>
</section>
