TEX := pdflatex -halt-on-error

TEXDEPS := $(wildcard *.tex) $(wildcard *.bib)
FIGDEPS := $(wildcard images/*)

all: $(TEXDEPS:.tex=.pdf)

%.pdf: %.tex $(FIGDEPS) Makefile
	$(TEX) $< && $(TEX) $<

clean:
	rm -f *.aux *.log *.out *.bbl *.blg
	rm -f rechenschaftsbericht.pdf
