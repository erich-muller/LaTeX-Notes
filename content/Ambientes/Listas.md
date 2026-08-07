---
title: 2.1 Listas
draft: false
tags:
order:
---
Para criar listas no seu documento, comumente você usará o **itemize** e o **enumerate**. 

- **itemize:** é um ambiente que te permite criar listas não enumeradas (estilo *bullet-points*).
- **enumerate:** similar ao itemize, mas cria listas ordenadas. Por padrão utiliza números, mas pode ser formatado de diversas formas.

Dentro desses ambientes é importante destacar quando começar um item, para isso usamos o comando `\item`.

Além disso, é possível ter ambientes aninhados. Veja o exemplo abaixo.


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

 ![[Pasted image 20260723145414.png]]

> [!check] Próxima página
> [[Figuras]]
