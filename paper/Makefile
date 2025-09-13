PAPER=paper.tex
TEXFILES=

TEX=latex
BIBTEX=bibtex

############################################################

.SUFFIXES: .tex .dvi .ps .pdf

all: $(PAPER:.tex=.pdf)

$(PAPER:.tex=.pdf): $(TEXFILES) $(PAPER:.tex=.bib)

.tex.pdf:
	pdf$(TEX) $<
	$(BIBTEX) $(PAPER:.tex=)
	pdf$(TEX) $<
	pdf$(TEX) $<

clean:
	rm -f *~ *.dvi *.ps *.log *.aux *.bbl *.blg
	rm -f comment.cut
	rm -f $(PAPER:.tex=.pdf)

.PHONY: clean

