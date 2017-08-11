all:
	xelatex example.tex
	evince example.pdf
template:
	xelatex template.tex
	evince template.pdf
jats2tex:
	jats2tex example.xml -t template.yaml
debug:
	JATS2TEX_DEBUG=1 jats2tex -w 0 example.xml -t template.yaml
