---
title: Primary index for Blog (Booklet level 1)
abstract:  |
    The web pages test specific aspects of web page construction, for example  

    - references,
    - images.

    The blog directory collects files to test most features of `daino`.

# author: AOS
date: Jan. 4, 2019
# indexPage: true
# todo is index page true necessary?
indexSort: filename
bibliography: resources/BibTexLatex.bib
# an index needs a biblio entry to cover included mds
book: "bookbig"   # "booklet" does not include text
keywords: test
version:  publish #  private  #
# visibility: public
---

# The Blog directory gives example for web page design v3

Each page shows a particular aspect of the design of a web page:

- pages in languages other than english,
- references in text from a standard bibliograhy,
- references with sources locally added,
- images

The pages serve as conventient test to check for the listed features. 

<!-- todo add booklet
 -->
# Explanation for *Index Pages* 

The index pages list automatically all the directories and the markdown files (`md` extension) in a directory.

The list gives first the subdirectories and then the files. The order for each of the two groups is determined by the value given for `indexSort`. Possible sort orders are:

- `filename` 
<!-- todo filename, but actually is title -->
- `date` or `reversedate`

For each directory it uses the YAML header of the sub-directory and shows:

- the title (from the `title` keyword^[The filename does not show in the list and can be used to achieve the desired order of items show by preceding the filenames with numerals, e.g. 001, 003, 010...])
- the abstract (from the `abstract` keyword)
- the date (from the `date` keyword)
- the author if it is not listed as a surpressed author in the `settings` file.



