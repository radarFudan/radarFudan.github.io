---
layout: post
title: "latex-notes"
date: 2021-02-06
---

Left parenthesis:
$$ = \left\{\begin{array}{lcl} ,& & {}\\ ,& & {} \end{array} \right.$$

The number of schemes choosing d balls from N+d elements
$${N+d \choose d}$$

Lots of symbols: 
[symbols](https://www.evanott.com/data-analysis/LaTeX/symbols.html)

How to insert pdf file at end of a Latex script
\usepackage[final]{pdfpages}
\includepdf[pages=-]{file.pdf} or \includepdf[pages=-,pagecommand={},width=\textwidth]{file.pdf}
[Original website](https://tex.stackexchange.com/questions/105589/insert-pdf-file-in-latex-document)

How to write algorithm part in LaTeX:
\usepackage[ruled,vlined]{algorithm2e}
\begin{algorithm}[H]
\SetAlgoLined
\KwResult{Write here the result }
 initialization\;
 \While{While condition}{
  instructions\;
  \eIf{condition}{
   instructions1\;
   instructions2\;
   }{
   instructions3\;
  }
 }
 \caption{How to write algorithms}
\end{algorithm}

Reference:
1. [Overleaf_website](https://www.overleaf.com/learn/latex/algorithms)