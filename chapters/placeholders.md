# Placeholders

Placeholders are used to insert additional content or variables in the document.
The syntax for placeholders is:

```
[[PLACEHOLDER]]

# Example
[[date]]
```

The most commonly used placeholders are:


| Placeholder                   | Meaning                                               |
| ----------------------------- | ----------------------------------------------------- |
| `[[TOC]][ordered=true/false]` | Inserts the table of contents at the current position |
| `[[BIB]]`                     | Inserts the bibliography list at the current position |
| `[[GLS]]`                     | Inserts the glossary list at the current position     |
| `[[date]]`                    | Inserts the current date                              |
| `[[time]]`                    | Inserts the current time                              |
| `[[datetime]]`                | Inserts the current date and time                     |
| `[[author]]`                  | Inserts the author of the document                    |
| `[[title]]`                   | Inserts the title of the document                     |
&nbsp;

Additionally all entries defined in the `custom_attributes` section of the configuration
can be inserted as placeholders.

