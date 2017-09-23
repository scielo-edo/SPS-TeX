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
      <fn fn-type="supplementary-material">
        <p>Trabalho baseado na tese de doutorado, de Capucho H. C., intitulada: “Sistemas manuscrito
          e informatizado de notificação voluntária de incidentes em saúde como base para a cultura
          de segurança do paciente”, apresentada à Escola de Enfermagem de Ribeirão Preto da
          Universidade de São Paulo, em 2012.</p>
      </fn>


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


