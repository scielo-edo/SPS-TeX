all:
	-rm LIVRO.pdf
	make clean
	latexmk -xelatex LIVRO.tex
scielo:
	sh convert-math-to-pdf.sh
	latexmk -quiet -interaction=nonstopmode -xelatex LIVRO.tex
	-rm LIVRO.pdf
	latexmk -quiet -interaction=nonstopmode -xelatex LIVRO.tex
clean:
	-rm *aux *log *tui *toc *.4ct *.4tc *.html *.css *.dvi *.epub *.lg *.ncx *.xref *.tmp *.idv *.opf  
	-rm -rf EBOOK-epub
	-rm -rf EBOOK-epub3
	-rm -rf EBOOK-mobi
debug:
	-rm LIVRO.pdf
	make clean
	latexmk -xelatex LIVRO.tex
	cp LIVRO.pdf ~/vmboxshared/LIVRO.pdf
	#evince LIVRO.pdf