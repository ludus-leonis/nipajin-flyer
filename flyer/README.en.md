# NIP'AJIN Shots

[Deutsch](README.md) | [English](README.en.md).

Please also read the license information in the root folder.

## Introduction

These leaflets are complete, self-contained Mini-RPGs on two A6 pages: one page rules, one page scenario.

## Quickstart

Each subdirectory contains all necessary files for one leaflet. Running

```
leaflet-name$ make en
```

will generate an English version of the leaflet (if available) as PDF into an `out` folder.

Other available languages can be found by looking into the `Makefile`.

## Translating leaflets

If you want to translate a leaflet, do:

* Copy `content.xx.tex` of your source language to `content.yy.tex`. `yy` is the ISO 639-1 code of your target language. If possible, use the German version, as this is the original one.
* Edit your `content.yy.tex` and translate all texts. Take care to use a UTF-8 editor, don't change intendations and don't translate the macro names.
* Edit the `Makefile`. Add a `VERSION_yy = ...` line for your language at the top and copy the target block of another language to use as temlate for yours and change it accordingly.
* When all is said and done, `make yy` will generate the new leaflet.
