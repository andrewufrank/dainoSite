---
title: No proprietary file formats
abstract: The source of the web site is formatted with common, non-proprietary formats. 
author: AOS
date: 2020-06-18
keywords: SSG
language: en_US
# todo how are the languages parsed. can there be a default
# publish: true
version: publish
visibility: public
# headerShift: one todo 
---

The source of the web site should be stored in open file formats, which can be exchanged and read by many programs. It should be easy to take a site organized with one SSG and put it into another one. Proprietary formats make it typically hard to extract content, store it in an open format, and to move it to another program --- effectively locking users in. 

The principle speaks against use of databases to store content (so called Content Management Systems) which are probably justified for large, very high traffic sites, a use case, `daino` is not design for. 

`Daino` organized the source for a web site in text files written in Markdown; they can be edited with any simple text editor^[Using a *intelligent* editor like Word is inconvenient; `VS code` however works well.].

