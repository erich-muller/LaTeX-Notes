---
title: 3.2 Referências Cruzadas
draft: false
tags:
---

Em trabalhos, é comum querer citar figuras, equações, seções, entre outros. Essa tarefa, apesar de simples, pode ser um gargalo em arquivos grandes. Por exemplo, se o seu trabalho tem 10 figuras e você precisar adicionar uma outra no começo do documento, todas as figuras abaixo mudam a numeração e consequentemente as referências à elas devem mudar. O $\LaTeX$ provém uma forma de fazer referências de forma automática que simplifica essa tarefa.

Para criar referências, tudo que precisamos é do par de comando `\label{}` e `\ref{}`. O comando `label` permite rotular partes do texto (dar um nome) para que a gente possa referenciar depois. O comando `ref` serve justamente para referenciar um `label` que fizemos anteriormente. Veja o exemplo abaixo:


 ```latex
 \section{Introdução} \label{introducao}
 
 A seguir, uma equação e uma figura.
 
 \begin{equation}
     e^{i\pi} + 1 = 0
     \label{relacao_euler}
 \end{equation}
 
 \begin{figure}[h]
     \includegraphics[width=\textwidth]{figura.jpg}
     \caption{Legenda da figura.}
     \label{paisagem}
 \end{figure}
 
 Na seção \ref{introducao} deste documento, criamos a equação \ref{relacao_euler} e a figura \ref{paisagem}.
 ```
 
 ![[Pasted image 20260723212018.png]]

Podemos também aplicar a teoremas, tabelas e várias outros ambientes dentro do $\LaTeX$. Futuramente, se inserirmos outra equação antes, figura ou seção, o $\LaTeX$ irá colocar o número correto automaticamente.

> [!tip] Dica
> Se você adicionar o pacote `hyperref`, todas as referências ficarão clicáveis. Assim, se houver uma menção à uma figura, ao clicar sobre o número você será levado diretamente a ela.

> [!bug] Cuidado ao nomear labels!
> labels devem ser nomeados de forma única. Definir dois ou mais labels com o mesmo nome pode gerar um conflito e consequentemente um erro na compilação.

> [!check] Próxima página
> [[Idioma]]