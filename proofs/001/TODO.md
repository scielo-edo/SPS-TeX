Fora do escopo de jats2tex
==========================

* Dividir artigos em dois arquivos como no PDF
* Falta de informação. Ex: Data de publicação incompleta.

Perguntas genéricas
-------------------

## Como evitar que uma definição abareça duas vezes sem obedecer o LaTeX. (\subject)

```
subject:
  head: |

    \edef{\subject}{@@children}
```

Questões pontuais
=================

Date
----

Criar uma forma de colocar a data conforma a língua


Instituição com ref dobrada
---------------------------

Tirar índice >>ao final<<

Output 
```
\author[I]{Capucho, Helaine Carneiro >>I<<}
\author[II]{Cassiani, Silvia Helena De Bortoli II}

\affil[I]{Departamento de Gestão e Incorporação de Tecnologias em
SaúdeSecretaria de Ciência, Tecnologia e Insumos
EstratégicosMinistério da Saúde}
\affil[II]{Departamento de Enfermagem Geral e
EspecializadaEscola de Enfermagem de Ribeirão PretoUniversidade de São Paulo}

```


yaml
```
aff:
  head: |
    \affil[@@lua(
      return find('//label')
    )@@]{@@lua(
      return find('//institution')
    )@@}

```

abstract-name vazio
-------------------

Quando abstract-name estiver vazio ignorar

```
abstract: |

  \renewcommand{\abstractname}{@@lua(return find "//title")@@}
  \begin{abstract}
  @@lua(return find "//p")@@
  \ifdef{\kwdgroup}{\kwdgroup}{}
  \end{abstract}
  %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

trans-abstract: |

  \renewcommand{\abstractname}{@@lua(return find "//title")@@}
  \begin{abstract}
  @@lua(return find "//p")@@
  \ifdef{\kwdgrouptrans}{\kwdgrouptrans}{}
  \end{abstract}
  %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
```


Title / Subtitle
----------------

<article-title xml:lang="pt"> 
	\title

<article-title xml:lang="en"> 
    \subtitle 

