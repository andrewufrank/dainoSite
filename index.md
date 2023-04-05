---
title: "Static Site Generator Daino: Landing page" 
abstract: The `Example Homepage` 
    produced by `daino` list differences to other SSG and gives rationale for its design. It points to the source and how to use it to run your own web site.
author: Author of Settings
date: 2010-01-29
keywords: homepage
# page-title: ExampleHomepage
version: publish
# visibility: public
---

#  Daino: A Static Site Generator 
<!-- copy of the ReadMe.md file shown in github -->

A static site generator designed by an academic to allow: 

- web pages written as (Pandoc) markdown (with YAML header for title and `bibtex` references, etc.),
- page layout inspired by Tufte and using `w3c` framework to adapt to different screen sizes,
- publication list for download produced from `bibtex` database,
- offer printable `pdf` files for all content; for some directories compilation from multiple pages on a single *booklet* page,
- web site using multiple languages, with support for common shortcuts for typing (e.g. ae is changed to ä when acceptable)
- content and appearances (theme) separated,
- a single `yaml` file for setup, and 
- a self-contained result which can be hosted on any web server.

## Software reuse:
Daino uses  `pandoc` and other packages on `Hackage` (e.g. shake, twitch, scotty)^[It was influenced by Chris Penner's [slick](https://github.com/ChrisPenner/slick#readme), newer, and seemingly simpler is [`Ema`](`https://github.com/srid/ema`) by  Sridhar Ratnakumar, but the documentation did not detail its features neither how it is built.].
Relies on `git` for version management and runs on PC(AMD) or Raspberry Pi 4 (ARM64) hardware.

## Example site
Thn example site [shown here](daino.gerastree.at) can be donloaded or clones   from [github](git clone git@github.com:andrewufrank/dainoSite). 

If `daino` can be installed from hackage or downloaded or cloned  from `git clone git@github.com:andrewufrank/daino.git` and installed with `cabal install` or `stack install`^[Initial compilation and linking brings in a large number of packages, e.g. pandoc, and may take a while; on a typically AMD computer 30..60 Minutes, on a ARM64 (e.g. RaspberryPi4) twice as long for the initial installation.].

To run the test site, start daino in it `dough` directory  `daino -qs`  and rendered in a browser as `localhost:3000`. The web pages written in markdown can be edited and the server restarted to update the site.

## Running your own site
Copying the folder `douch` to a suitable directory and edit the `settinsNN.yaml` file found there is enough to start your own site with running `daini -qs` in this directory.  

# More information: 

The following pages explain the rationale for "yet another static site generator" and show with examples how it can be used. 