# Dossiers
CODE := $(shell pwd)
PDFDIR = ../_pdf/4_quatrieme
THEME = 

# Visualiser les pdf
LOG=evince

# Créer le dossier pdf s'il n'éxiste pas.
target:
	test -d $(PDFDIR) || mkdir $(PDFDIR)

all: img poly proper

# Générations des images
FIGSRC = $(wildcard 4x1-pythagore/sources/*.ipe 4x2-trigonometrie/sources/*.ipe 4x6-thales/sources/*ipe)

FIGOBJ = $(FIGSRC:.ipe=.pdf)

img: $(FIGOBJ)

4x1-pythagore/sources/%.pdf: 4x1-pythagore/sources/%.ipe
	ipetoipe -pdf $<
	
4x2-trigonometrie/sources/%.pdf: 4x2-trigonometrie/sources/%.ipe
	ipetoipe -pdf $<

4x6-thales/sources/%.pdf: 4x6-thales/sources/%.ipe
	ipetoipe -pdf $<	

# Chapitre 1 - Nombres relatifs 1

1_cours:
	pdflatex 4x1-nombres-relatifs-1/4x1-nombres-relatifs-1.tex
	pdflatex 4x1-nombres-relatifs-1/4x1-nombres-relatifs-1.tex
	mv 4x1-nombres-relatifs-1.pdf '$(PDFDIR)'/4x1-nombres-relatifs-1.pdf
	
1_ie:
	pdflatex 4x1-nombres-relatifs-1/4x1-nombres-relatifs-1-ie.tex
	pdflatex 4x1-nombres-relatifs-1/4x1-nombres-relatifs-1-ie.tex
	mv 4x1-nombres-relatifs-1-ie.pdf '$(PDFDIR)'/4x1-nombres-relatifs-1-ie.pdf

# nettoyage			
proper:
	rm -f *.log *.toc *.aux *.nav *.snm *.out *.bbl *.blg *.dvi
	rm -f *.backup *~