# Bibliography

Snekdown Supports Bibliography entries and references similar to BibTex.

Definition:
```
[SD_GITHUB]: https://github.com/trivernis/snekdown
[SD_BOOK]:[type=book, author=Snek, title = "Snekdown Book" date="08/20/2020", publisher=Snek]
```

[SD_GITHUB]: https://github.com/trivernis/snekdown
[SD_BOOK]:[type=book author=Snek, title = "Snekdown Book", date="08/20/2020" publisher="Snek "]

The definitions of bibliography entries are not rendered. Instead the `[[BIB]]` placeholder 
must be used to insert a table of bibliography entries. Only entries that are used in the document are rendered.

[[BIB]]

To reference a bib entry, use the `[^KEY]` syntax. For example:
`[^SD_BOOK]`.
This renders as [^SD_BOOK].


The numbers are assigned based on first occurrence.
```
There is a book about snekdown[^SD_BOOK] and a github repo[^SD_GITHUB].
```

There is a book about snekdown[^SD_BOOK] and a github repo[^SD_GITHUB].


The bibliography handling is provided by the [Bibliographix](https://github.com/Trivernis/bibliographix) crate.
Supported types are:


| Type          | Required Fields                               | Optional Fields                                    |
| ------------- | --------------------------------------------- | -------------------------------------------------- |
| article       | key, author, title, journal, date             | volume, number, pages, url                         |
| book          | key, author, title, publisher, date           | volume, series, address, edition, url              |
| booklet       | key, title                                    | author, how_published, address, date               |
| in_book       | key, author, title, position, publisher, date | volume, series, address, edition                   |
| in_collection | key, author, title, publisher, date           | editor, volume, series, position, address, edition |
| manual        | key, title                                    | author, organization, address, edition, date       |
| misc          | key                                           | author, title, date, url, how_published            |
| repository    | key, author, title                            | url, cms, license, accessed_at                     |
| tech_report   | key, author, title, institution, date         | number, address                                    |
| thesis        | key, author, title, school, date              | address                                            |
| unpublished   | key, author, title                            | date                                               |
| website       | key, url                                      | title, author, accessed_at, date                   |

&nbsp;
Bibliography can also be defined in a separate TOML file with the following syntax:

```toml
# Bibliography.toml
[BIB_KEY]
key = "value"

[SD_BOOK]
type = "book"
author = "Snek"
title = "Snekdown Book"
date = "20.08.2020"
publisher = "Snek"

[SD_GITHUB]
type = "website"
url = "https://github.com/trivernis/snekdown"
```
&nbsp;

