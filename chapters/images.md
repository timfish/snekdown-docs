# Image Syntax

Simple Syntax
`!(url)`


Extended syntax with a description
`![description](url)`


Extended syntax with metadata to specify the size
`![description](url)[metadata]?`


Extended syntax with metadata and no description
`!(url)[metadata]`


When generating the html file the images are base64 embedded. To turn off this behaviour
set the config parameter `embed-external` to `false`.


## Manipulation

With the provided metadata images can be manipulated:


![Original](img/snek.png)[width=20%]
|| `![Original](img/snek.png)[width=20%]`


![Grayscale](img/snek.png)[width=20% grayscale]
|| `![Grayscale](img/snek.png)[width=20% grayscale]`

![Invert](img/snek.png)[width=20% invert]
|| `![Grayscale](img/snek.png)[width=20% invert]`


![Hue Shift](img/snek.png)[width=20% huerotate=90]
|| `![Hue Shift](img/snek.png)[width=20% huerotate=90]`


![Adjust Brightness](img/snek.png)[width=20% brightness=100]
|| `![Adjust Brightness](img/snek.png)[width=20% brightness=100]`


![Adjust Contrast](img/snek.png)[width=20% contrast=50]
|| `![Adjust Contrast](img/snek.png)[width=20% contrast=50]`


The image manipulations can also be combined. The order of execution can not be changed.


![Cursed](img/snek.png)[width=20% grayscale invert huerotate=90 brightness=100 contrast=50]
|| `![Cursed](img/snek.png)[width=20% grayscale invert huerotate=90 brightness=100 contrast=50]`