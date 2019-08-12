# Dossiers
CODE := $(shell pwd)
PDFDIR = ../_pdf/3_troisieme
THEME = 

# Visualiser les pdf
LOG=evince

# Créer le dossier pdf s'il n'éxiste pas.
target:
	test -d $(PDFDIR) || mkdir $(PDFDIR)

all: img poly proper

# Générations des images
FIGSRC = $(wildcard 4x1-pythagore/sources/*.ipe 4x2-pythagore/sources/*.ipe 3xx-dm/sources/dm1/*.ipe)

FIGOBJ = $(FIGSRC:.ipe=.pdf)

img: $(FIGOBJ)

4x1-pythagore/sources/%.pdf: 4x1-pythagore/sources/%.ipe
	ipetoipe -pdf $<

3xx-dm/sources/dm1/%.pdf: 3xx-dm/sources/dm1/%.ipe
	ipetoipe -pdf $<

# Chapitre 1 - Probabilité

3x1:
	pdflatex 3x1-probabilite/3x1-proba.tex
	pdflatex 3x1-probabilite/3x1-proba.tex
	mv 3x1-proba.pdf '$(PDFDIR)'/3x1-proba.pdf
	


# nettoyage			
proper:
	rm -f *.log *.toc *.aux *.nav *.snm *.out *.bbl *.blg *.dvi
	rm -f *.backup *~
	