TAG=0034-8910-rsp-48-01-0094

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
update:
	-cp Makefile ..
	-cp template.yaml ..
upgrade:
	-cp ../template.yaml .

