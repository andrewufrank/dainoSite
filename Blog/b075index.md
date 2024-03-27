---
title: "b075:index"
abstract: The index file collects an index for some terms and prints with the page numbers.
author: AOS
date: 20230314
keywords: test
version: publish
# visibility: public
---

# Collect an index v23

At appropriate positions add `\index{key}`, for example `\index{index1}` \index{index1}. 

## Preparation 
>To enable the indexing feature of LaTeX, the makeidx package must be loaded in the preamble with:

    \usepackage{makeidx}

>and the special indexing commands must be enabled by putting the

    \makeindex

\index{prepare!index}

At the end of the document, to show the index within the document, merely use the command

    \printindex


