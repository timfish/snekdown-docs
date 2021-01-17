# Imports

A key feature of Snekdown is splitting a document
into several files and importing those files in the main
document.

Additionally files that provide Glossary entries, Bibliography, Style and
Configurations can be imported with the same syntax.

```
<[path]

# import another snekdown document at the current position
<[document.md]

# import a stylesheet that will be embedded in the document
<[style.css][type=stylesheet]

# import a configuration file
<[Manifest.toml]

# import bibliography
<[MyBib.toml][type=bibliography]

# import a glossary

<[MyGls.toml][type=glossary]
```

The parser differentiates five different types of imported files.

- `document` - The default import which is just another Snekdown document
- `stylesheet` - CSS Stylesheets that are included when rendering
- `bibliography` - A file including bibliography
- `config/manifest` - A config file that contains metadata
- `glossary` - Glossary entries

Imports of Snekdown documents are parsed in a separate thread, so you
might see a performance improvement when splitting a large document into
several files.