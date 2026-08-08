---
title: 2.1 Listas
draft: false
tags:
order:
---
Para criar listas no seu documento, comumente você usará o ambiente **itemize** ou o **enumerate**. 

- **itemize:** é um ambiente que te permite criar listas não enumeradas (estilo *bullet-points*, como esse).
- **enumerate:** similar ao itemize, mas cria listas ordenadas. Por padrão utiliza números, mas pode ser formatado de diversas formas.

Dentro desses ambientes é importante destacar quando começar um item, para isso usamos o comando `\item`. Além disso, é possível ter ambientes aninhados. Veja o exemplo abaixo.


 ```latex
 \documentclass{article}
 
 \begin{document}
 
 Essa é uma lista enumerada.
 \begin{enumerate}
     \item Maçã
     \item Banana
     \item Pera
 \end{enumerate}
 
 \
 
 Essa é uma lista não enumerada.
 \begin{itemize}
     \item Banana prata
     \item Banana caturra
     \item Banana ouro
 \end{itemize}
 
 \
 
 Aqui estamos aninhando duas listas.
 \begin{enumerate}
     \item Maçã
     \item Banana
     \begin{itemize}
         \item Banana prata
         \item Banana caturra
         \item Banana ouro
     \end{itemize}
     \item Pera
 \end{enumerate}
 
 \end{document}
 ```

 ![[Pasted image 20260723145414.png | 500]]


---

# Customizando ambientes enumerados

Para ambientes enumerados, é possível trocar a forma de enumeração, seja usando números indo-arábicos, romanos ou letras do alfabeto. Para isso, é necessário adicionar `\usepackage{enumerate}` no preâmbulo do seu documento.

Essencialmente, para modificar o comportamento do `enumerate` basta adicionar um parâmetro opcional indicando o formato desejado usando `1` para números indo-arábicos, `I` para números romanos, `a` para letras minúsculas e `A` para letras maiúsculas. Veja o exemplo abaixo.

```latex
\documentclass{article}
\usepackage{enumerate}

\begin{document}

Enumeração indo-arábica:
\begin{enumerate}[1)]
    \item Primeiro item
    \item Segundo item
    \item Terceiro item
\end{enumerate}

\

Enumeração romana:
\begin{enumerate}[(I)]
    \item Primeiro item
    \item Segundo item
    \item Terceiro item
\end{enumerate}

\

Enumeração alfabética (minúsculas):
\begin{enumerate}[a.]
    \item Primeiro item
    \item Segundo item
    \item Terceiro item
\end{enumerate}

\ 

Enumeração alfabética (maiúsculas):
\begin{enumerate}[A -]
    \item Primeiro item
    \item Segundo item
    \item Terceiro item
\end{enumerate}

\end{document}
```

![[Figuras/Pasted image 20260808170446.png]]

> [!check] Próxima página
> [[Figuras]]
