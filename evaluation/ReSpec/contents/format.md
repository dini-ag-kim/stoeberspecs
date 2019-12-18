## Format

A service card holds general information about an application as well as further information about provided services (e. g. interfaces for search, harvesting, tools).

A service card MUST be represented by a JSON object. This JSON object MUST have some mandatory properties and MAY have some optional properties described <a href="#vocabulary">below</a>.

An application's service card MUST be provided in the format JSON-LD as a standalone JSON file or embedded in the application's homepage.

If the service card is provided as a standalone JSON file the `Content-Type` header MUST be set to `application/ld+json`:

```
Content-Type: application/ld+json
```

The service card MUST be referenced in one of the following ways.

1. A `script` tag containing the service card's JSON object MUST be placed in the `head` section of the homepage:

   ```
    <script type="application/ld+json">[...]</script>
   ```

OR

2. A `link` tag referencing the service card's JSON file MUST be placed in the `head` section of the homepage:

   ```
   <link rel="meta" type="application/ld+json" href="[...]" title="Service-Description" />
   ```

OR

3. A `Link` header referencing the service card's JSON file MUST be sent along with the homepage:

   ```
   HTTP/1.1 200 OK
   Link: <[...]>; rel="meta"
   ```
