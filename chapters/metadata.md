# Metadata / Element Attributes

Metadata or element attributes are a way to change the behaviour of some
elements.

The syntax for metadata is the same syntax used for defining keys of bibliography entries
in the document.

```
String value
[key = value]

String value
[key = "String value"]

Integer value
[key = 123]

Float value
[key = 1.23]

Boolean
[key = false]
[key] equals [key=true]
```

There are some elements that support metadata:

```
Hide a section (including subsections) in the TOC
#[toc-hidden] Section

Set the size of an image
!(url)[width = 42%, height=auto, brightness=10, contrast=1.2, huerotate=180, invert, grayscale]

Set the source of a quote
[author=Me date=[[date]] display="{{author}} - {{date}}"]> It's me

Set options for placeholders
[[toc]][ordered]

Set the type of an import
<[style.css][type=stylesheet]
```
&nbsp;
