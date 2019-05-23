# (c) 2009-2016 by Markus Leupold-Löwenthal
# This file is released under CC BY-SA 4.0. Please do not apply other licenses one-way.

PDF_NAME = "NIPAJIN-Flyer-Small-Fry"
TEX_NAME = "flyer"
VERSION_DE = $(shell grep Version}{ content.de.tex | sed -e "s/.*{//;s/}.*//")
VERSION_EN = $(shell grep Version}{ content.en.tex | sed -e "s/.*{//;s/}.*//")
VERSION_PL = $(shell grep Version}{ content.pl.tex | sed -e "s/.*{//;s/}.*//")

default: de

all: de en pl

setup:
	mkdir -p out
	ln -sf ../../nipajin.sty out/nipajin.sty
	ln -sf ../../flyer.sty out/flyer.sty

images: setup
	ln -sf ../images out/images

de: images
	ln -sf ../flyer.tex out/flyer.tex
	ln -sf ../../core/rules.de.tex out/rules.tex
	ln -sf ../content.de.tex out/content.tex
	xelatex \
		-output-driver="xdvipdfmx -V 5 -z 9" \
		-jobname=${PDF_NAME}-de-${VERSION_DE} \
		-output-directory out ${TEX_NAME}

en: setup images
	ln -sf ../flyer.tex out/flyer.tex
	ln -sf ../../core/rules.en.tex out/rules.tex
	ln -sf ../content.en.tex out/content.tex
	xelatex \
		-output-driver="xdvipdfmx -V 5 -z 9" \
		-jobname=${PDF_NAME}-en-${VERSION_EN} \
		-output-directory out ${TEX_NAME}

pl: setup images
	ln -sf ../flyer.tex out/flyer.tex
	ln -sf ../../core/rules.pl.tex out/rules.tex
	ln -sf ../content.pl.tex out/content.tex
	xelatex \
		-output-driver="xdvipdfmx -V 5 -z 9" \
		-jobname=${PDF_NAME}-pl-${VERSION_PL} \
		-output-directory out ${TEX_NAME}

clean:
	rm -rf out/*
