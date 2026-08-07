---
title: 1.4 Símbolos Matemáticos
draft: false
tags:
order:
---

Existem diversas formas de escrever matemática em ambientes $\LaTeX$. Alguns comandos matemáticos que veremos a seguir não vêm nativamente no $\LaTeX$, para importá-los basta usar o comando `\usepackage{...}` no preâmbulo (começo do documento). Para esses exemplos usaremos o pacote **amsmath**. Assim, no início do documento, inclua `\usepackage{amsmath}`. 

### Matemática in-line e full-line

Texto matemático dentro de um parágrafo é digitado entre `\(` e `\)`, entre `$` e `$` ou entre `\begin{math}` e `\end{math}`.

> [!example] Exemplo 
> ```latex
> \TeX{} é pronunciado como $\tau\epsilon\chi$.
> $a^{2} + b^{2} = c^{2}$
> Isto vem do meu $\heartsuit$
> ```
> 
> $\TeX{}$ é pronunciado como $\tau\epsilon\chi$.
> $a^{2} + b^{2} = c^{2}$
> Isto vem do meu $\heartsuit$

Para grandes equações é preferível usar linhas separadas. Para isso, basta escrever entre `\[` e `\]`, entre `$$` e `$$` ou entre `\begin{displaymath}` e `\end{displaymath}`. Note ainda que esses ambientes exibem equações de forma distinta ao caso anterior. Veja o exemplo abaixo.

> [!example] Exemplo
> ```latex
> $\lim_{n \to \infty} \sum_{k=1}^n \frac{1}{k^2} = \frac{\pi^2}{6}$
> ```
> 
> $\lim_{n \to \infty} \sum_{k=1}^n \frac{1}{k^2} = \frac{\pi^2}{6}$
> 
> ---
> 
> ```latex
> $$\lim_{n \to \infty} \sum_{k=1}^n \frac{1}{k^2} = \frac{\pi^2}{6}$$
> ```
> 
> $$\lim\limits_{n \to \infty} \sum\limits_{k=1}^n \dfrac{1}{k^2} = \dfrac{\pi^2}{6}$$

> Existem muitos símbolos matemáticos e por isso não colocaremos todos aqui. Para um guia completo use https://lief.if.ufrgs.br/pub/latex/lshortBR.pdf (página 55).


> [!todo]- Exercício
> Escreva um código em $\LaTeX$ com a seguinte saída:
> 
> ![[Pasted image 20260723175849.png]]

### Textos Matemáticos

Vale ressaltar que dentro do ambiente matemático todo texto é tratado como variável. Assim, ao escrever `$pelo Teorema 1$`, obtemos "$pelo Teorema 1$". Para escrever textos dentro de ambientes matemáticos usamos o comando `\text{}`. Também podemos usar `\textbf{}` ou `\textit{}` para textos em negrito ou itálico.

Há ainda alguns outros textos matemáticos que são estilizados. A seguir, algumas formas de se obter esses resultados.

| Exemplo               | Comando               | Pacote necessário          |
| --------------------- | --------------------- | -------------------------- |
| $\mathrm{ABCdef}$     | `\mathrm{ABCdef}`     | ❌                          |
| $\mathit{ABCdef}$     | `\mathit{ABCdef}`     | ❌                          |
| $\mathnormal{ABCdef}$ | `\mathnormal{ABCdef}` | ❌                          |
| $\mathcal{ABC}$       | `\mathcal{ABC}`       | eucal com a opção: mathcal |
| $\mathscr{ABC}$       | `\mathscr{ABC}`       | eucal com a opção: mathscr |
| $\mathfrak{ABCdef}$   | `\mathfrak{ABCdef}`   | eufrak                     |
| $\mathbb{ABC}$        | `\mathbb{ABC}`        | amsfonts ou amssymb        |

> [!tip] Dica
> Para criar equações enumeradas ou agrupadas, consulte [[Equações Enumeradas]]. Para construir matrizes, funções por partes ou tabelas, consulte [[Alinhamento Vertical]]. Para organizar teoremas, definições automaticamente, veja [[Teoremas, Definições, etc.]].


> [!check] Próxima página
> [[Imagens]]
