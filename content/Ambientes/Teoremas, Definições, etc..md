---
title: 2.5 Teoremas, Definições, etc.
draft: false
tags:
order:
---
O $\LaTeX$ possui uma ferramenta que te ajuda a organizar teoremas, corolários e outros. Para criar essas estruturas usamos o código `\newtheorem{NOME}{TEXTO}` no preâmbulo do documento. Apesar do nome "theorem" esse código permite criar qualquer estrutura, como axiomas, proposições, etc. O parâmetro `NOME` é como vamos chamar o ambiente e `TEXTO` é o que vai aparecer quando esse ambiente for usado. Vamos criar um exemplo com definição e teorema.

```latex
\documentclass{article}

\newtheorem{definicao}{Definição}
\newtheorem{teorema}{Teorema}

\begin{document}

\begin{definicao}
    Retângulo é um quadrilátero que possui os ângulos internos retos.
\end{definicao}

\begin{definicao}
    Quadrado é um polígono regular com 4 lados.
\end{definicao}

\begin{teorema}
    Todo quadrado é um retângulo.
\end{teorema}

\begin{teorema}[Teorema de Pitágoras]
Se um triângulo retângulo tem catetos medindo $a$ e $b$ e a hipotenusa mede $c$, então
$$a^2 + b^2 = c^2$$
\end{teorema}

\end{document}
```
![[Pasted image 20260724134257.png]]


> [!todo]- Exercício
> Com base nos ambientes vistos até aqui, modifique o arquivo `Exercicio 4.tex` para que ele tenha a seguinte aparência.
> 
> ![[Figuras/Pasted image 20260808182017.png]]


> [!check] Próxima página
> [[Referências/index|Referências]]