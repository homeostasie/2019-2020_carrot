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

# Chapitre 2 - Proportionnalité 1

# Chapitre 3 - Puissances

3_cours:
	pdflatex 4x3-puissances/4x3-puissances.tex
	pdflatex 4x3-puissances/4x3-puissances.tex
	mv 4x3-puissances.pdf '$(PDFDIR)'/4x3-puissances.pdf
	
3_exo:
	pdflatex 4x3-puissances/4x3-puissances-exo.tex
	pdflatex 4x3-puissances/4x3-puissances-exo.tex
	mv 4x3-puissances-exo.pdf '$(PDFDIR)'/4x3-puissances-exo.pdf

3_ie:
	pdflatex 4x3-puissances/4x3-puissances-ie.tex
	pdflatex 4x3-puissances/4x3-puissances-ie.tex
	mv 4x3-puissances-ie.pdf '$(PDFDIR)'/4x3-puissances-ie.pdf	

# Chapitre 4 - Pythagore

4_ie:
	pdflatex 4x4-pythagore/4x4-pythagore-ie.tex
	pdflatex 4x4-pythagore/4x4-pythagore-ie.tex
	mv 4x4-pythagore-ie.pdf '$(PDFDIR)'/4x4-pythagore-ie.pdf	


# Chapitre 5 - Expression litterale

5_eq:
	pdflatex 4x5-calcul-litteral-1/4x5-calcul-litteral-eq.tex
	pdflatex 4x5-calcul-litteral-1/4x5-calcul-litteral-eq.tex
	mv 4x5-calcul-litteral-eq.pdf '$(PDFDIR)'/4x5-calcul-litteral-eq.pdf


5_cours:
	pdflatex 4x5-calcul-litteral-1/4x5-calcul-litteral.tex
	pdflatex 4x5-calcul-litteral-1/4x5-calcul-litteral.tex
	mv 4x5-calcul-litteral.pdf '$(PDFDIR)'/4x5-calcul-litteral.pdf

5_pp:
	pdflatex 4x5-calcul-litteral-1/4x5-calcul-litteral-pp.tex
	pdflatex 4x5-calcul-litteral-1/4x5-calcul-litteral-pp.tex
	mv 4x5-calcul-litteral-pp.pdf '$(PDFDIR)'/4x5-calcul-litteral-pp.pdf


5_ns:
	pdflatex 4x5-calcul-litteral-1/4x5-calcul-litteral-ns.tex
	pdflatex 4x5-calcul-litteral-1/4x5-calcul-litteral-ns.tex
	mv 4x5-calcul-litteral-ns.pdf '$(PDFDIR)'/4x5-calcul-litteral-ns.pdf

5_sci:
	pdflatex 4x5-calcul-litteral-1/4x5-calcul-litteral-sci.tex
	pdflatex 4x5-calcul-litteral-1/4x5-calcul-litteral-sci.tex
	mv 4x5-calcul-litteral-sci.pdf '$(PDFDIR)'/4x5-calcul-litteral-sci.pdf	
# nettoyage			
proper:
	rm -f *.log *.toc *.aux *.nav *.snm *.out *.bbl *.blg *.dvi
	rm -f *.backup *~