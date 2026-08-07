---
title: 1.3 Seções, Subseções e outros
draft: false
tags:
order:
---
Comumente em textos científicos precisamos dividir o conteúdo. Em documentos do tipo "article" (artigo), faremos isso através de seções e subseções.

Para criar uma seção, basta usar o comando `\section{Nome da Seção}`. O $\LaTeX$ automaticamente irá enumerar todas as seções do seu documento. Caso você queira uma seção sem numeração, basta usar o comando `\section*{Seção sem número}`. Em geral, o caractere "\*" sempre é usado para remover a enumeração automática de ambientes.

Dentro de seções é possível criar subseções com o comando `\subsection{Nome da Subseção}`. A numeração da subseção dependerá da seção que ela estiver contida.


 ```latex
 \documentclass{article}
 
 \begin{document}
 
 \section{Minha primeira seção}
 Aqui vai um texto dentro da primeira seção.
 
 \subsection{Esta é uma subseção}
 Aqui podemos colocar mais texto.
 
 
 \section*{Seção não enumerada}
 As seções não enumeradas não interferem na contagem. Assim, a próxima seção enumerada será a seção 2.
 
 \section{Outra Seção}
 
 \end{document}
 ```
 
 ![[Pasted image 20260722165143.png|578]]


> [!todo]- Exercício 
> Crie um código em $\LaTeX$ que gere o seguinte resultado.
> 
> ![[Pasted image 20260722174126.png ]]


Aqui vem uma das grandes comodidades do $\LaTeX$. Dado que todas as seções serão processadas pelo compilador, podemos criar um sumário de forma automatizada. Para isso, usamos o comando `\tableofcontents`.


 ```latex
 \documentclass{article}
 
 \begin{document}
 
 \tableofcontents
 
 \newpage
 
 \section{Minha primeira seção}
 Aqui vai um texto dentro da primeira seção.
 
 \subsection{Esta é uma subseção}
 Aqui podemos colocar mais texto.
 
 \section*{Seção não enumerada}
 As seções não enumeradas não interferem na contagem. Assim, a próxima seção enumerada será a seção 2.
 
 \section{Outra Seção}
 
 \end{document}
 ```
 
 ![[Pasted image 20260723143149.png]]

> [!bug] Cuidado!
> Note que no exemplo acima a seção não enumerada não aparece no sumário. Qualquer ambiente não enumerado não constará em listas de índices.

> [!check] Próxima página
> [[Símbolos Matemáticos]]