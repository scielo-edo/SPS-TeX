


disp-formula/mml:math  -->  mathml
inline-formula/mml:math  -->  mathml

disp-formula/tex-math  -->  formula latex (\label{e1}  
    \ref{e1} <disp-formula[@xref="e1"]>)




Done
====

* 157 artigo & testes
* Sistema compatível com Xpath

* editing.sh
    * quebras & espaços?

Principais avanços
------------------

<fig>
    * tratamento de imagens
    * formatos
    * quebra de edição

<inside-graphic>

<disp-quote>

<list>

<ref>

<ref-group>

<fn>
    * Dúvida: é preciso ter sempre @id?

* Imagens
* Links
* Penalidades
* Reconhecimento da língua ??

Fazer ainda
-----------

* Novo template
* Tabela fixa
* Duas colunas
* [XX] nas ref
* Estilo em vírgulas nas notas. 
* Estaços em branco


Duvidas com Pedro
----------------

```
abstract/sec/title: "\\section{@@children}"

abstract: |
  
    \ifdef{\abstracttitle}{\renewcommand{\abstractname}{\abstracttitle}}{}
  
    \begin{abstract}
    @@lua(return "\\newcommand{\\abstracttitle}{" .. find('abstract/title') .. "}")@@
    @@lua(return find "//p")@@
    \ifdef{\kwdgroup}{\kwdgroup}{}
    \end{abstract}
```


Milestone
=========

https://github.com/scielo-edo/SPS-TeX/tree/hello/proofs/001


Fora do escopo de jats2tex
==========================

* Falta de informação. Ex: Data de publicação incompleta.

