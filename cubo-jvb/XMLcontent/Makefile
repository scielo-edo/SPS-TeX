all:
	-rm test.pdf
	make clean
	latexmk -xelatex test.tex
hello:
	-rm hello.pdf
	make clean
	latexmk -xelatex hello.tex
clean:
	-rm *.aux *.fls *.fdb_latexmk *.log *.bib *.blg *.bbl *.ltx *.run.xml
