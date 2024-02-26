---
title: levels of titles  
abstract: An example blog title and a long, multi-line abstract   
    without fixed line breaks and footnotess  
# author: AOS
date: 2020-06-18
# keywords: Blog
# language: en_US
# todo how are the languages parsed. can there be a default
# publish: true
version: publish
# visibility: public
# headerShift: one
---

# level1 Titel
Some nonsense text under level 1^[Technically, it will be rendered as level 2 title, given that the title is level1.]

A title must not be included in *"* or *'*, otherwise the production of pdf files does not work.^[Problem with the `\section` tex command.]

## level2 Two with tests for footnotes
<!-- Some text with two footnotes in a row.^[First footnote]^[second footnote]. Known but -  does not work, see [https://github.com/jgm/pandoc/issues/8652] -->

Same with indidviudal notes.[^one][^two]

[^one]: first note.
[^two]: second note. 

    This footnote has a second paragraph. 

<!-- A an inline footnote cannot have a second paragraph^[First line.

    This could be the second line for the footnote]

with the continuation of the text  -->

### level3 
The tufte style does discourage the use of multiple levels of titles; the styles for the levels 3, 4 and 5 do not have sensible defaults and should be adapted^[Probably in the `theme/templates/static/tufte-additions.css` file] if intended to be used!


#### level 4
textfor level 4
##### level 5
Text at level 5 are slightly indented in pdf but not in html. Is this a good idea

if level 5 produces a latex error, then likely are the limitations on depth limit in the file `usr/local/texlive/2023/texmf-dist/tex/latex/tufte-latex/tufte-common.def`  not commented out.

To show list, references and images are explained in the next examples.[^long]

[^long]: This is a footnote which is too long and contains much text to fill space and interact with the next title; a second sentence without no other intentions as filling space.

# level 1 titel very very very very very very  but not yet long enogh title

This title must^[footnote test to check interaction]not interfere with footnote above or later.

# footnotes

The commonmark style is [^one] but not allowing inline footnote, which are convenient^[a second short footnote inline] and are easier to write - but partially more disturbing when revising a document.

The current version `daino68` is again using Pandoc markdown; `daino67` was the experiment with commonmark. 