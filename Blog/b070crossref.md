---
title: "07 Crossreferences"
abstract: A cross-reference is a reference from one part of the text to another.
author: AOS
date: Jan. 4, 2019
keywords: test
version: publish
# visibility: public
---

# Problem: HTML and PDF produces 

Commonmark allows multiple methods to define a marker

# A {refA}
## refB {refB}
### refC
## <a name="tith"></a> tith

# A reference within the same file 

These markers can be used to include a reference in a text: 

    alternative [seeHash](#refA)  
    fuer hinten [seeB](#refB)  
    fuer hinten - wegen klammer doppel [seeBB](#refb-refb) geht aber geschweifte klammer nicht, 
    fuer hintenC [seeC](#refc)  funktioniert ohne klammer
    versuch drei [seeTith](#tith)  funktioniert

alternative [seeHash](#refA)  
fuer hinten [seeB](#refB)  
fuer hinten - wegen klammer doppel [seeBB](#refb-refb) funktioniert,  
fuer hintenC [seeC](#refc)  funktioniert ohne klammer
versuch drei [seeTith](#tith)  funktioniert

wrong markers understand the text as a file and fail to find it:

    some text [see](refA) sucht file   
    versuch zwei [see2](a-refa) sucht file  
    versuch vier [seeNoHash](tith) sucht file    


# A reference to another file

Requires for HTML a full file name plus the marker within the text:

    [html chapter1 focus2](/BookExample/01part/01_1_chapter.html#focus2)

and see for html [html chapter1 focus2](/BookExample/01part/01_1_chapter.html#focus2)

Unfortunately, latex sees this and produces `\href{/BookExample/01part/01_1_chapter.html\#focus2}{html chapter1 focus2}` which points to the html and not the pdf output. If no extension is set, then pandoc completes with  `pdf`. But then, pandoc when producing the html does not correspond. 

for latex: and see for html [html chapter1 focus2](/BookExample/01part/01_1_chapter#focus2) points in the pdf to another pdf file.

with the extension, points in html to the pdf file and see for html [html chapter1 focus2](/BookExample/01part/01_1_chapter.pdf#focus2)


# Referencing in books and booklets PDDF

In books and booklets multiple files are merged to produce a single `tex` file which is then processed by latex in one go. 

pandoc inserts labels for sections: 

    \section{section 1 of c1 one hash title}\label{section-1-of-c1-one-hash-title}

which can later be used to produce a reference to the page with `\pageref{level3}` for example: see page \pageref{level3}


todo which pages are used hyperef, varioref and cleveref [https://en.wikibooks.org/wiki/LaTeX/Labels_and_Cross-referencing]
