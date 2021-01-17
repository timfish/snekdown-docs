# Glossary

You can use glossary entries in Snekdown to provide
a way of linking abbreviations to their longer form
and auto expand the first occurrence of an abbreviation.


Glossary entries can be defined in a separate TOML File.
Per default the `Glossary.toml` file gets imported.

```toml
# Glossary.toml

[SHORT]
long = "Long Form"
description = "The description of the entry"

# Example
[HTML]
long = "Hypertext Markup Language"
description = "The markup language of the web"
```

The defined entries can be used in the text by using the following syntax:


Short entry:
```
~SHORT
~HTML
```

~SHORT
~HTML


The first occurrence expands to the long form. When using it a second time it uses the shorter form:

~SHORT
~HTML


You can force Snekdown to use the long form for an entry by writing

```
~~SHORT
~~HTML
```

~~SHORT
~~HTML


The list of glossary entries can be inserted with the `[[GLS]]` placeholder.

[[GLS]]