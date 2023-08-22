---
title: 
    titleb030title.md  *02alltext* with two space to break  
    here. Issue - inserts `<p>` before the text with the 
    break, which then overwrites the text size in tufte.

abstract: |
    abstract02 missing with two spaces  
    here in two lines  
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
doNotReplace: blue true koeffizient einbauen "ä" "ö" "ü"
---

# Title must have " to include :

This is a rule of YAML, which reads the header.

Linebreaks in the YAML header are forced by two returns (a single return has no effect). 

Der fixe Zeilenumbruch im Abstract ist nicht günstig für die automatische Anpassung an die Schirmgrösse.
