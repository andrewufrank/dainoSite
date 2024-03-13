---
abstract: 
    a  example abstract broken with /lf/
    in lines /lf/
    third line. /lf/
    blank lines (even with two spaces)  
    do not break /lf/ 
    # test for enumeration /lf/  
    # = a line /lf/
    # = another /lf/
    # the summary could be ..

title: title broken with  / lf / here not permitted

date: 2020-06-18
# keywords: Blog
# language: en_US
# todo how are the languages parsed. can there be a default
# publish: true
version: publish
# visibility: public
# headerShift: one
---

linebreaks in abstract can be simulated with /lf/ marks. Attention:
spaces before necessary! but not in title.

## abstract wtih enumerations
the better solution is the one in b001blog.md

<!-- enumerations do not work in abstracts. simmulate with `=` (not `-`).

test again after switch to commonmark. -->

## break lines in titles 
Not to break titles into lines is a limitation of latex: 

[https://tex.stackexchange.com/questions/43431/how-to-make-force-line-break-in-chapter-title-in-toc-chapter-header-if-p]

    The standard class page headers are really only set up for one line. If doing it a lot you should modify the page headers to set the mark text into a parbox, but for a one-off long entry you can put the parbox into the mark. So this breaks all three instances:

    \chapter[medium-length\\ title for TOC, if wanted]{full\\ title name}
    \chaptermark{\protect\parbox{.5\textwidth}{short title\\ for running headers}}

