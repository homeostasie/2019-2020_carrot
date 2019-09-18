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

3x1-ie:
	pdflatex 3x1-probabilite/3x1-proba-ie.tex
	pdflatex 3x1-probabilite/3x1-proba-ie.tex
	mv 3x1-proba-ie.pdf '$(PDFDIR)'/3x1-proba-ie.pdf

3x1-exo:
	pdflatex 3x1-probabilite/3x1-exercices.tex
	pdflatex 3x1-probabilite/3x1-exercices.tex
	mv 3x1-exercices.pdf '$(PDFDIR)'/3x1-exercices.pdf
	
3x1-pb:
	pdflatex 3x1-probabilite/3x1-problemes.tex
	pdflatex 3x1-probabilite/3x1-problemes.tex
	mv 3x1-problemes.pdf '$(PDFDIR)'/3x1-problemes.pdf

# nettoyage			
proper:
	rm -f *.log *.toc *.aux *.nav *.snm *.out *.bbl *.blg *.dvi
	rm -f *.backup *~
	