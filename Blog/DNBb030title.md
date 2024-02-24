---
title:
    titleb030title.md 03titleBroken with /lf/ to break. breaks index
abstract: |    
    Issue was that  literal block as title inserts `<p>` before the text with the
    break, which then overwrites the text size in tufte. 

    breaking with   two spaces  
    here which do not break in two lines
    NL mit einenm Doppelpunkt im Titel (innerhalb Anführungszeichen)

    NL und mit einem ä im Abstract

    und weiteren Zeilen im abstract
    mit einem fixen Zeilenumbruch und einer liste


    = eins (ein strichlein, plus oder stern geht verloren!)


    = zwei
    

    ende abstract

    alternativ

    - eins
    - zwei

    mit liste

author: Peter Beispiel
date: 2020-06-18
# keywords: Blog
language: de_CH
version: publish
# visibility: public
# headerShift: one
bibliography: resources/BibTexLatex.bib
# reference-section-title: Literatur
doNotReplace: blue true koeffizient einbauen "ä" "ö" "ü" issue
---

# Title must have " to include :

This is a rule of YAML, which reads the header.

Linebreaks in the YAML header are forced by two returns (a single return has no effect).

Der fixe Zeilenumbruch im Abstract ist nicht günstig für die automatische Anpassung an die Schirmgrösse.
