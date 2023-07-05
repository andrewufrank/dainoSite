---
title: "Static Site Generator `Daino`: Landing page" 
abstract: The `Example Homepage` 
    produced by `daino` lists differences to other SSG and gives the rationale for its design. `Daino` is built the Unix-style from existing tools. The site explains how to use it to run your own web site.
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

The program runs on Debian Linux^[Could run on Ubuntu or likely Windows(probably some adaptations needed).] locally on a PC or Raspery Pi 4.

Restricted accsss on some directories is achieved using the server^[My provider uses `cpanel` and allows password protection to any directory.].

## Software reuse:
Daino uses  `pandoc` and other packages on `Hackage` (e.g. shake, twitch, scotty)^[It was influenced by Chris Penner's [slick](https://github.com/ChrisPenner/slick#readme), newer, and seemingly simpler is [`Ema`](`https://github.com/srid/ema`) by  Sridhar Ratnakumar, but the documentation did not detail its features neither how it is built.].

It relies on `git` for version management and Debian Linux.

## Example site
The example site [shown here](daino.gerastree.at) contains more information how to build a site with `daino`.

`Daino` can be installed from hackage or downloaded or cloned  from `git clone https://github.com/andrewufrank/daino.git` and installed with `cabal install` or `stack install`^[Initial compilation and linking brings in a large number of packages, e.g. Pandoc, and may take a while; on a typically AMD computer 30..60 Minutes, on a ARM64 (e.g. RaspberryPi4) twice as long for the initial installation.].

The example site can be downloaded or cloned   from `github` with `git clone https://github.com/andrewufrank/dainoSite.git`. In the `settings3.yaml` file replace `/home/frank/dainoTest_1_5_2` three times with the path to the directory which contains the test site.

To run the test site, start daino in this directory with  `daino -qs`  and render the result in a browser by opening `localhost:3000`. The web pages written in markdown can be edited and the server restarted to update the site.^[Producing the pdf files as well with `daino -s` may produce some messages pointing to the latex logs; can usually be ignored.]

## Running your own site
Copying the the test site to a suitable directory and edit the   
`settinsNN.yaml`^[Currently `settings3.yaml`] 
file found there is enough to start your own site with running `daino -qs` in this directory. 

Delete the `.git` directory in the copy and restart git with `git init` to obtain version management for your site.

# More information: 

The `ReadMe` in the test site  explain the rationale for "yet another static site generator" and show with examples how it can be used. The Blog directory contains instructive examples of specific uses and serves as test pages to check processing.