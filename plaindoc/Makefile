latexfile = doc
texengine = xelatex

$(latexfile).pdf: *.tex refs.bib
	$(texengine) $(latexfile)
	bibtex $(latexfile)
	while ($(texengine) $(latexfile) ; \
	grep -q "Rerun to get" $(latexfile).log ) do true ; \
	done
	rm -fr auto *.aux *.log *.aux *.bbl *.blg *.out *.toc

view:	$(latexfile).pdf
	open $(latexfile).pdf

clean:	
	rm -fr auto *.aux *.log *.aux *.bbl *.blg *.out *.toc *.pdf
