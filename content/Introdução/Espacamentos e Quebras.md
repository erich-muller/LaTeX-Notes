---
title: 1.2 Espaçamentos e Quebras
draft: false
tags:
order:
---


O $\LaTeX$, por padrão, ignora espaçamentos e quebras de linhas repetidas.

 Veja que no documento abaixo os espaços repetidos foram desconsiderados. Além disso, pular 2 linhas ou mais criou um novo parágrafo, mas uma única quebra de linha não surtiu efeito.
 
 ```latex
 \documentclass{article}
 
 \begin{document}
 Minha           terra tem     palmeiras,          
 Onde  canta      o Sabiá;
 
 
 
 As aves, que aqui gorjeiam, 
 
 Não gorjeiam como lá.
 \end{document}
 ```
 ![[Pasted image 20260723140955.png]]

Para criar espaços adicionais é necessário usar a barra invertida "\\". 
Para quebrar linhas você pode usar a barra invertida entre linhas vazias. No exemplo abaixo foi dado um espaço entre "Minha" e "Terra"; 3 espaços entre "o" e "Sabiá" e quebramos 2 linhas no meio do poema.

 ```latex
 \documentclass{article}
 
 \begin{document}
 Minha \ terra tem palmeiras,          
 Onde canta o \ \ \ Sabiá;
 
 \
 
 \
 
 As aves, que aqui gorjeiam, 
 Não gorjeiam como lá.
 \end{document}
 ```
 
 ![[Pasted image 20260723142115.png]]

Para **quebrar uma página inteira** você pode usar o comando `\newpage`.

> [!check] Próxima página
> [[secoes subsecoes e outros | Seções, Subseções e outros]]