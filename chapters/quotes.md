# Quotes

Snekdown supports standard markdown quotes with `>` and quotes with additional metadata:

Simple (default) Syntax:
```
> This is a quote
```
> This is a quote


Multiline Quotes:
```md
> This is a 
> Multiline Quote
```
> This is a 
> Multiline Quote

You can even add additional metadata to quotes, like the autor or year:
```md
[author=Trivernis year=2020 display='{{author}} - {{year}}']> This is a quote with metadata
```
[author=Trivernis year=2020 display='{{author}} - {{year}}']> This is a quote with metadata