# Configuration

Some attributes of a Snekdown document can be controlled by using a configuration file.
The default name for this file is `Manifest.toml`. When importing a `toml` file, it gets interpreted
as a configuration file by default. Multiple configurations are combined.


The basic layout of the manifest file is the following:
```toml
# document metadata
[metadata]

# features used in the document
[features]

# additional imports and blacklists
[imports]

# settings related to pdf rendering
[pdf]

# image settings
[images]

# Visual adjustments
[style]

# custom metadata
# String -> String Mappings
[custom_attributes]
```

## Metadata

    The metadata sections allows for configuration of document metadata.
It currently supports two keys:

```toml
[metadata]
# Language setting of the document
language = 'en'

# Author of the document
author = 'author'

# Title of the document
title = 'title'

# A short description for the document preview
description = '''
Description
'''

# Keywords to find the document
keywords = ['HTML', 'Snekdown']
```


## Features

The features section provides options to turn off some snekdown features.
The provided options are:

```toml
[features]

# if external sources (images, stylesheets, MathJax)
# should be embedded into the document (default: true)
embed_external = true

# If SmartArrows should be used (default: true)
smart_arrows = true

# If the MathJax Library should be included.
# Without this library the math rendered by snekdown won't be displayed
# correctly in browsers that don't support MathML (for example Chromium based browsers).
# (default: true)
include_mathjax = true
```


## Imports

The import section allows the definition of additional imports and imports that
should be ignored.

```toml
[imports]
# those files won't get imported
ignored_imports = []

# stylesheets that should be included
included_stylesheets = ['style.css']

# bibliography that should be included
included_bibliography = ['Bibliography.toml']

# glossary that should be included
included_glossaries = ['Glossary.toml']
```


## PDF

In the pdf section, some settings related to the PDF Rendering can be tweaked.

```toml
[pdf]

# If the header and footer of the pdf should be displayed (default: true)
display_header_footer = true

# PDF header template of each page (default: '<div></div>')
header_template = '<div></div>'

# PDF footer template of each page (default: the value below)
footer_template = '''
<div style="font-size: 10px; text-align: center; width: 100%;">
    <span class="pageNumber"></span>/<span class="totalPages"></span>
</div>'''

# The scale at which the website is rendered into pdf.
page_scale = 1.0

# Margin of the document
[pdf.margin]

# Top margin of the pdf. Should be between 0 and 1. (default: 0.5)
top = 0.5

# Bottom margin of the pdf. Should be between 0 and 1. (default: 0.5)
bottom = 0.5

# Left margin of the pdf. Should be between 0 and 1.
left = 0

# Right margin of the pdf. Should be between 0 and 1.
right = 0
```


## Images

If you want to change the format or size of embedded images you can 
do so in this section.


```toml

# Force convert images to the specified format.
# Supported formats are png, jpeg, gif, bmp, (ico needs size <= 256), avif, pnm
# (default: keep original)
format = "png"

# the max width for the images.
# if an image is larger than that it gets resized.
# (default: none)
max_width = 700

# the max height for the images.
# if an image is larger than that it gets resized.
# (default: none)
max_height = 500
```


## Style

The style section provides options to tweak the visual appearance of
the Snekdown document.


```toml
[style]
# how bibliography references should be displayed
bib_ref_display = '{{number}}'

# the chosen theme for the document
# one of: GithubLight, SolarizedLight, OceanLight, SolarizedDark, OceanDark, MagicDark
theme = 'GithubLight'
```


## Custom Attributes

The custom_attributes section can be used to define custom keys
that can be inserted as placeholders in the document. The mapping has to be
a String -> String mapping.

```toml
[custom_attributes]
custom_key1 = "Custom Value"
```
&nbsp;
