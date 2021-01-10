# Math

Math annotations can be created with the [AsciiMath](http://asciimath.org/) Syntax.
The parser is implemented in it's own crate [asciimath-rs](https://github.com/Trivernis/asciimath-rs).

Inline math:
```md
Inline math $$ a^2 + b^2 = c^2 $$ in one line.
```
Inline math $$ a^2 + b^2 = c^2 $$ in one line.


Block Math:
```
$$$
A = [[1, 2],[3,4]]
$$$
```
$$$
A = [[1, 2],[3,4]]
$$$
&nbsp;

Snekdown uses [MathJax](https://www.mathjax.org/) for improving the output of rendered MathML expressions.
Browsers like Firefox support rendering of MathML directly so it's not a requirement to use it there. It can be turned off with the feature setting `include_mathjax`.