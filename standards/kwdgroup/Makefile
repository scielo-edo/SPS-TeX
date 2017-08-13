TAG=kwdgroup

all:
	jats2tex $(TAG).xml -t template.yaml
	cat $(TAG).tex
debug:
	JATS2TEX_DEBUG=1 jats2tex -w 0 $(TAG).xml -t template.yaml

