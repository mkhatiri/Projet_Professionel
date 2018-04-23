DOC := projet_recherche_bleuse

ifeq ($(wildcard /usr/include/LaTeX.mk),/usr/include/LaTeX.mk)
LU_MASTERS := $(DOC)
include LaTeX.mk
else

SHELL := /bin/bash

all: pdf

pdf: $(DOC).pdf

$(DOC).pdf: $(DOC).tex
	pdflatex $<
	bibtex $(DOC)
	pdflatex $<
	pdflatex $<

clean:
	rm -f $(DOC).{aux,log,nav,out,snm,pdf,toc,vrb,ps,dvi,bbl,blg}

endif
