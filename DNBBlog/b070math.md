---
title: "07 Include Math "
abstract: This example shows how code math!
author: AOS
date: Jan. 4, 2019
keywords: test
version: publish
# visibility: public
---

# This example shows the inclusion of latex math code

nonsense text  $\alpha$-times   and $\epsilon$ in single dollar characters. The next line brackets the formula with a single dollar character 

$G* = (1-\epsilon) \times (\alpha - 1) \div (\alpha)$

and then with two 

$$G* = (1-\epsilon) \times (\alpha - 1) \div (\alpha)$$

und eine Formel im Text $(\alpha - 1) \div (\alpha)$ eingefuegt.

in footnote[^foot1] ok?

[^foot1]: hier $\pi$  und $(\alpha - 1) \times (\alpha)$. 

Problems encountered with formula in footnote like here.[^foot2]

[^foot2]: Footnote with some text and a formula 

    $G* = (1-\epsilon) \times (\alpha - 1) \div (\alpha)$

    to demonstrate. 





convert markdown with freestanding pandoc: 

- pandoc -s --mathml -i math4two.md  -o math4two.html
- pandoc -s --pdf-engine=lualatex -i math4two.md  -o math4two.pdf

Rules:
Anything between two $ characters will be treated as TeX math. The opening $ must have a non-space character immediately to its right, while the closing $ must have a non-space character immediately to its left, and must not be followed immediately by a digit. Thus, $20,000 and $30,000 won’t parse as math. If for some reason you need to enclose text in literal $ characters, backslash-escape them and they won’t be treated as math delimiters.
