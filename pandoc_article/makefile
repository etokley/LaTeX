all: ms.pdf

ms.pdf:	ms.md refs.bib template.tex
	pandoc -s -S ms.md -o ms.pdf --bibliography=refs.bib --csl=jneurophysiol.csl --template=template.tex --latex-engine=xelatex

clean:	
	rm -f ms.pdf
