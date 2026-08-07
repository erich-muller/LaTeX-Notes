---
title: 2.2 Figuras
draft: false
tags:
order:
---
Por vezes, é importante enumerar as figuras e inserir legendas. O ambiente `figure` permite que o usuário tenha acesso a esses recursos e outros mais com facilidade. O exemplo abaixo mostra como fazer isso. Para criar a legenda da figura, foi necessário adicionar o comando `\caption{}`.

 ```latex
 \begin{figure}
    \includegraphics[width=\textwidth]{figura.jpg}
   \caption{Legenda da figura.}
\end{figure}
 ```
 
 ![[Figuras/Pasted image 20260723190651.png]]

> Caso queira sua figura centralizada, use `\centering` dentro do ambiente `figure`. 

> [!bug] Figuras fora do lugar
> Talvez a sua figura não apareça no PDF na mesma posição que está no seu código. Isso ocorre pois o $\LaTeX$, por padrão, renderiza figuras sempre no início de páginas. Para consertar isso, basta escrever `\begin{figure}[h]`. O parâmetro `h` indica para o compilador que a figura deve ser renderizada nessa parte do texto (do inglês, "here"). Em casos de erro você pode forçar esse comportamento usando `\begin{figure}[!h]`.

### Subfiguras

Também é possível criar subfiguras, cada uma com a sua legenda. Para tal, é necessário adicionar 2 pacotes: `\usepackage{caption}` e `\usepackage{subcaption}`.

Veja um exemplo de como inserir subfiguras.

```latex
\begin{figure}
     \centering
     \begin{subfigure}[b]{0.3\textwidth}
         \centering
         \includegraphics[width=\textwidth]{graph1}
         \caption{$y=x$}
         \label{fig:y equals x}
     \end{subfigure}
     \hfill
     \begin{subfigure}[b]{0.3\textwidth}
         \centering
         \includegraphics[width=\textwidth]{graph2}
         \caption{$y=3\sin x$}
         \label{fig:three sin x}
     \end{subfigure}
     \hfill
     \begin{subfigure}[b]{0.3\textwidth}
         \centering
         \includegraphics[width=\textwidth]{graph3}
         \caption{$y=5/x$}
         \label{fig:five over x}
     \end{subfigure}
        \caption{Three simple graphs}
        \label{fig:three graphs}
\end{figure}
```

![[Figuras/Pasted image 20260723191314.png]]


> [!tip] Dica
> Você pode criar um sumário das suas figuras automaticamente digitando `\listoffigures`.

> [!check] Próxima página
> [[Equações Enumeradas]]