# (c) 2019 by Markus Leupold-Löwenthal
# This file is released under CC BY-SA 4.0. Please do not apply other licenses one-way.

PDF_NAME = "NIPAJIN-Flyer-Goblins"
TEX_NAME = "flyer"
VERSION_DE = $(shell grep Version}{ content.de.tex | sed -e "s/.*{//;s/}.*//")

default: de

all: de

setup:
	mkdir -p out
	ln -sf ../../nipajin.sty out/nipajin.sty
	ln -sf ../../flyer.sty out/flyer.sty

images: setup
	ln -sf ../../images out/images

de: images
	ln -sf ../flyer.tex out/flyer.tex
	ln -sf ../../core/rules.de.tex out/rules.tex
	ln -sf ../content.de.tex out/content.tex
	xelatex \
		-output-driver="xdvipdfmx -V 5 -z 9" \
		-jobname=${PDF_NAME}-de-${VERSION_DE} \
		-output-directory out ${TEX_NAME}

clean:
	rm -rf out/*
