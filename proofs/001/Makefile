TAG=0034-8910-rsp-47-04-0791

all:
	jats2tex $(TAG).xml -t template.yaml
	cat $(TAG).tex

2:
	jats2tex $(TAG).xml -t template2.yaml
	cat $(TAG).tex

debug:
	JATS2TEX_DEBUG=1 jats2tex -w 0 $(TAG).xml -t template.yaml

sublime:
	subl3 -n . $(TAG).xml $(TAG).tex template.yaml Makefile

pdf:
	xelatex $(TAG).tex
	evince $(TAG).pdf

pdf-modelo:
	evince MODELO.pdf

git:
	-git add .
	-git commit -m "General edition"

clean:
	-rm *.aux *.log

