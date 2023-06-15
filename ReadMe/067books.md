---
title: Produce books
abstract: From a bunch of blog-sized posts a booklet or a book should be produced in a printable, i.e. `pdf` format.
author: AOS
date: 2023-04-05
keywords: SSG
language: en_US
# todo how are the languages parsed. can there be a default
# publish: true
version: publish
# visibility: public
# headerShift: one todo 
# doNotReplace: "ae" "oe" "ue" 
---

A collection of blog posts, a.k.a. `md` files a comprehensive printable version should be produced. 

It is based on the construction of the index pages, which include automatically all `md` files in the directory in which the `index.md` file is placed. 

Marking the `yaml header` of the index file with 

    book: booklet 

or

    book: bookbig

a comprehensive file for the directory, respectively for the `bookbig` case, the diretory and its subdirectories, which must be marked with `booklet`, is produced. It uses `part` and `chapter` for two levels of titles above the `section` title marked with 

    title: someText 

in the `yaml header`. The single markdown header marker `#` is interpreted as `subsection`.

For `bookbig` and `booklet` table of content is automatically produced. 

