---
title: 2.3 Equações Enumeradas
draft: false
tags:
order:
---
Vejamos alguns ambientes especiais que possuem características próprias. Os ambientes abaixo te ajudam a alinhar o seu texto, numerar e quebrar linhas com facilidade. Use diferentes ambientes para diferentes necessidades.

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
> Crie um documento com a seguinte aparência.
> 
> ![[Pasted image 20260723182143.png]]

> [!check] Próxima página
> [[Alinhamento Vertical]]