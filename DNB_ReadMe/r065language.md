---
title: Help with language specific input
abstract: Various conventions to speed up textual input exist and can be supported; currently support for german text input is built in.
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

In the `yaml header` of a markdown file the language must be specified if not U.S. english (marked as `en_US). I use often `de_CH` for the Swiss variants of german.

Various conventions to type text in non-english languages exist. For example, it is customary to type combinations of American keyboard characters to stand in for those which are not found on the standard American keyboard.
For example, when typing a German text, often the umlaut ä, ö and ü are written as "ae", "oe" and "ue". Unfortunately, it is not possible to just use a global replace, because some German words contain some such combinations (e.g. Koeffizienten) which must not be written as Köffizienten!
Similar conventions exist in other languages to type, e.g. email on standard keyboards. Italians, for example, replace an accented character with a appended apostrophe (italianita').

Daino includes a support program for german language writing which is automatically applied to German texts and replaces umlauts when acceptable. It uses a small list to guide the process, which is not perfect. Omissions can be edited manually and are not affected by later replacements. Commissions must be - on a file by file base - collected in type YAML header as `doNotReplace` list^[Specifically useful to allow some english words, like "blue", in a German text!]. Such a list remains with the file and need only updated when text is added and the replacement process produces undesired changes.

