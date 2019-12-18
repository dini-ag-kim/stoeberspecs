## Vocabulary

The normative vocabularies for service cards are [[schema.org]] and [[LRMI]]. The complete sub-set of properties used for service cards is described in this section.

For each property a short description, the degree if obligation (`mandatory`, `optional`), the data type and - if applicable - the range of allowed values is given.

<section data-dfn-for="@context">

### <dfn>@context</dfn>

This holds the JSON-LD context as a reference. This MUST be `https://schema.org/`.

<dl>
    <dt>Obligation</dt>
    <dd>mandatory</dd>
    <dt>Data Type</dt>
    <dd>`String` holding one URI</dd>
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
    <dd>`String` holding one URL</dd>
</dl>

</section>

<section data-dfn-for="type">

### <dfn>type</dfn>

The type of the application described by the service card. This MUST be `https://schema.org/WebSite` and `https://schema.org/Service`.

<dl>
    <dt>Obligation</dt>
    <dd>mandatory</dd>
    <dt>Data Type</dt>
    <dd>`String[]` holding one or more URI</dd>
    <dt>Values</dt>
    <dd>`https://schema.org/WebSite` and `https://schema.org/Service`</dd>
</dl>

</section>

<section data-dfn-for="name">

### <dfn>name</dfn>

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

An icon for the service. This MAY be used by third-party applications implementing the service.

<dl>
    <dt>Obligation</dt>
    <dd>optional</dd>
    <dt>Data Type</dt>
    <dd>`String` holding one URL</dd>
    <dt>Values</dt>
    <dd>Format: `svg` or `png`<br>Size: 64x64px</dd>
</dl>

</section>

<section data-dfn-for="logo">

### <dfn>logo</dfn>

A logo for the application or service. This MAY also be the logo of the hosting institution or other provider.

<dl>
    <dt>Obligation</dt>
    <dd>optional</dd>
    <dt>Data Type</dt>
    <dd>`String` holding one URL</dd>
</dl>

</section>

<section data-dfn-for="inLanguage">

### <dfn>inLanguage</dfn>

The primary language(s) of the content provided by the service. If given, this MUST be one or more of [[IETFBCP47]].

<dl>
    <dt>Obligation</dt>
    <dd>optional</dd>
    <dt>Data Type</dt>
    <dd>`String[]` holding one or more language tags</dd>
    <dt>Values</dt>
    <dd>[[IETFBCP47]]</dd>
</dl>

</section>

<section data-dfn-for="description">

### <dfn>description</dfn>

A short description of the application or service.

<dl>
    <dt>Obligation</dt>
    <dd>optional</dd>
    <dt>Data Type</dt>
    <dd>`String`</dd>
</dl>

</section>

<section data-dfn-for="serviceType">

### <dfn>serviceType</dfn>

The type(s) of service provided by the application. This MAY be one or more *Service subtype* of [[schema.org]], `Repository`, `Referatory`, `Wiki`, `LMS`.

<dl>
    <dt>Obligation</dt>
    <dd>mandatory</dd>
    <dt>Data Type</dt>
    <dd>`String[]`</dd>
    <dt>Values</dt>
    <dd><a href="http://schema.org/Service#subtypes">Subtypes of http://schema.org/Service</a>, `Repository`, `Referatory`, `Wiki`, `LMS` or any other</dd>
</dl>

</section>

<section data-dfn-for="audience">

### <dfn>audience</dfn>

The target audience for the application. If given, this MUST be one or more *Educational Audience Role* of [[LRMI]].

<dl>
    <dt>Obligation</dt>
    <dd>optional</dd>
    <dt>Data Type</dt>
    <dd>`String[]` holding one or more URI</dd>
    <dt>Values</dt>
    <dd><a href="http://purl.org/dcx/lrmi-vocabs/educationalAudienceRole/">LRMI Educational Audience Roles</a></dd>
</dl>

</section>

<section data-dfn-for="about">

### <dfn>about</dfn>

The subject(s) or topic(s) of resources provided by the application. This MAY be one or more *Thing subtype* of [[schema.org]].

<dl>
    <dt>Obligation</dt>
    <dd>optional</dd>
    <dt>Data Type</dt>
    <dd>`String[]` holding one or more URI</dd>
    <dt>Values</dt>
    <dd><a href="http://schema.org/Thing#subtypes">Subtypes of http://schema.org/Thing</a> or any other URI</dd>
</dl>

</section>

<section data-dfn-for="isAccessibleForFree">

### <dfn>isAccessibleForFree</dfn>

Can the application and it's services be used without authentication?

<dl>
    <dt>Obligation</dt>
    <dd>optional</dd>
    <dt>Data Type</dt>
    <dd>`Boolean`</dd>
</dl>

</section>

<section data-dfn-for="provider">

### <dfn>providery</dfn>

The provider of the application. This MUST be one or more JSON object with at least a `type` and `name` property. More properties MAY be given, e. g. `email`, `location`, `url`.

<dl>
    <dt>Obligation</dt>
    <dd>mandatory</dd>
    <dt>Data Type</dd>
    <dd>`Object[]`</dd>
    <dt>Values</dt>
    <dd>Object with at least a `type` and `name` property</dd>
</dl>

</section>

<section data-dfn-for="startDate">

### <dfn>startDate</dfn>

The launch date of the application. If given, this MUST conform with [[ISO8601]].

<dl>
    <dt>Obligation</dt>
    <dd>optional</dd>
    <dt>Data Type</dt>
    <dd>`Date`</dd>
    <dt>Values</dt>
    <dd>[[ISO8601]]</dd>
</dl>

</section>

<section data-dfn-for="availableChannel">

### <dfn>availableChannel</dfn>

This describes the services provided by the application. This MUST be one or more JSON object describing a `ServiceChannel` and `WebAPI` according to [[schema.org]].

<dl>
    <dt>Obligation</dt>
    <dd>mandatory</dd>
    <dt>Data Type</dt>
    <dd>`Object[]` holding one or more `Service` object</dd>
    <dt>Values</dt>
    <dd>Object of types <a href="https://schema.org/ServiceChannel">ServiceChannel</a> and <a href="https://schema.org/WebAPI">WebAPI</a></dd>
</dl>

</section>

<section data-dfn-for="schemaVersion">

### <dfn>schemaVersion</dfn>

The schema version of the service card.

<dl>
    <dt>Obligation</dt>
    <dd>mandatory</dd>
    <dt>Data Type</dt>
    <dd>`String` holding one URI</dd>
</dl>

</section>

<section data-dfn-for="dateModified">

### <dfn>dateModified</dfn>

The last modification date of the service card. This MUST conform with [[ISO8601]].

<dl>
    <dt>Obligation</dt>
    <dd>mandatory</dd>
    <dt>Data Type</dt>
    <dd>`Date`</dd>
    <dt>Values</dt>
    <dd>[[ISO8601]]</dd>
</dl>

</section>

<section data-dfn-for="license">

### <dfn>license</dfn>

The license(s) for the resources provided by the application.

<dl>
    <dt>Obligation</dt>
    <dd>optional</dd>
    <dt>Date Type</dt>
    <dd>`String[]` holding one or more URI</dd>
</dl>

</section>

<section data-dfn-for="sameAs">

### <dfn>sameAs</dfn>

Related websites for the application.

<dl>
    <dt>Obligation</dt>
    <dd>optional</dd>
    <dt>Data Type</dt>
    <dd>`String[]` holding one or more URL</dd>
</dl>

</section>
