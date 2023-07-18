---
title: 'The "002layout"  example: colons and quotes'  
abstract: 
    "An non-working example   abstract with fixed line breaks writen with escaped backslash n.\n\n    
    Note: \n
    - a title with `colon` requires quotes and \n

    - how to format a list in abstract. "
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

Rules for the YAML header are strict. After the keyword follows a colon and then a text. This text MUST NOT contain a colon (":") or set in quotes (single or double).

To have a line break add two blanks  
second line  
third line.  
Unfortunately this is not easily visible  
and pandoc markdown specific (adding a "\" at end of line does not help!).

A formatted list:
- first
- second 