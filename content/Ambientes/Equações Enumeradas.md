---
title: 2.4 Equações Enumeradas
draft: false
tags:
order:
---
Muito comumente é necessário enumerar equações, fórmulas e outros para que, posteriormente possamos referenciá-las. A seguir, veremos alguns ambientes dentro do $\LaTeX$ que nos permite fazer esse controle automaticamente. 

O primeiro ambiente é o `equation`. Ele enumera suas equações e também as alinha ao centro. Experimente o exemplo abaixo.

```latex
\begin{equation}
    f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!}(x-a)^n
\end{equation}
```

Esse ambiente, apesar de útil, não permite a quebra de linhas. Para isso, podemos usar um outro ambiente dentro do `equation`, conhecido como `split`. Esse outro ambiente não é nativo, portanto para conseguir usá-lo, certifique-se de adicionar `\usepackage{amsmath}` no seu preâmbulo. O exemplo abaixo mostra uma equação com mais de uma linha.

```latex
\begin{equation}
\begin{split}
    f(x) &= \sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!}(x-a)^n \\
    &= f(a) + \frac{f'(a)}{1!}(x-a) + \frac{f''(a)}{2!}(x-a)^2 + \dots
\end{split}
\end{equation}
```

Existem também outros ambientes para inserir equações que nativamente permitem quebras de linhas e fazem alinhamentos adequados. Você deve usar diferentes ambientes para diferentes necessidades, veja a tabela abaixo.

| ambiente | colunas | enumeração                       | quebra de linhas | alinhamento                                                                                                      |
| -------- | ------- | -------------------------------- | :--------------: | ---------------------------------------------------------------------------------------------------------------- |
| equation | 1       | um número para toda a expressão. |        ❌         | central                                                                                                          |
| eqnarray | 3       | um número para cada linha.       |        ✅         | esquerda, centro e direita.                                                                                      |
| align    | várias  | um número para cada linha        |        ✅         | alterna entre esquerda, centro e direita                                                                         |
| multline | 1       | um número para toda a expressão. |        ✅         | a primeira linha é alinhada à esquerda, as demais são alinhadas ao centro e a última linha é alinhada à direita. |
> Você pode omitir a numeração de um ambiente colocando um asterisco após o nome. Exemplo: `\begin{equation*} ... \end{equation*}`.

A seguir um exemplo para ver esses diferentes ambientes em ação.

 ```latex
 \documentclass{article}
 \usepackage{amsmath}
 
 \begin{document}
 
 \begin{equation}
     f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h} 
 \end{equation}
 
 \begin{eqnarray}
     2x-5y &= 8 \\
     x + 3y &= 10
 \end{eqnarray}
 
 \begin{align}
     x&=y & 2x&=-y & -4 + 5x&=2+y \\
 10 w &=z & 3w&=\frac{1}{2}z & w+2&=-1+w \\
 11 a&=b+c & a&=b & ab&=cb
 \end{align}
 
 \begin{multline}
     p(x) = \frac{\partial (x^5 + 22xy^3 -3xy)}{\partial x
  \partial y} + 3x^6 + 14x^5y + 590x^4y^2 + 19x^3y^3 -
  \\\ln | 3x - 32xy | + \int_0^\infty (\sqrt{xy + x^2} -
  x^5 + 2)\,dx\\ - 12x^2y^4 - 12xy^5 + 2y^6 - a^3b^3 -
  \ln | 90x^4y^2 + 19x^3y^3 |
 \end{multline}
 
 \end{document}
 ```
  ![[Pasted image 20260723160112.png]]


> [!todo]- Exercício
> Modifique o arquivo `Exercicio 3.tex` para que ele fique com a seguinte aparência.
> 
> ![[Figuras/Pasted image 20260814141559.png]]

> [!check] Próxima página
> [[Teoremas, Definições, etc.]]