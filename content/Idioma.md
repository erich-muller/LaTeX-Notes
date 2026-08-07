---
title: 4. Idioma
draft: false
tags:
---

Veja que as nomenclaturas automáticas são sempre feitas em inglês. As figuras estão nomeadas como "Figure", as referências estão como "References", mas não é isso que queremos quando estamos criando em documentos em Português. Para alterar esse comportamento é simples, basta usar o pacote `babel` com o parâmetro `brazil`.

```latex
\documentclass{article}
\usepackage{graphicx}
\usepackage[alf]{abntex2cite}
\usepackage[brazil]{babel}

\begin{document}

\tableofcontents 

\

\hrule

\section{Introdução} 

\LaTeX é um sistema computacional de editoração \cite{lamport1994}. De acordo com \citeonline{silva2023}, tecnologias favorecem a educação.

\section{Exemplos}

Abaixo, temos uma figura.

\begin{figure}[h]
    \centering
    \includegraphics[width=0.5\linewidth]{figura.jpg}
    \caption{Legenda da figura}
\end{figure}

\hrule

\addcontentsline{toc}{section}{Referências}
\bibliography{referencias}

\end{document}
```

 ![[Figuras/Pasted image 20260724112148.png | 700]]
