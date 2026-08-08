---
title: 2.3 Alinhamento
draft: false
tags:
order:
---
Os parágrafos no LaTeX são por padrão justificados, ou seja, nivelados com as margens esquerda e direita. Se você quiser alterar o alinhamento de um parágrafo, o LaTeX possui três ambientes: `center`, `flushleft` e `flushright`.

```latex
\documentclass{article}
\begin{document}

\begin{flushleft}
Esse texto ficará à esquerda.
\end{flushleft}

\begin{flushright}
Esse texto ficará à direita.
\end{flushright}

\begin{center}
Esse texto ficará ao centro.
\end{center}

\end{document}
```

![[Figuras/Pasted image 20260808144141.png]]

---
## Alinhamento em Matemática

Há casos em que é necessário criar sistemas de equações ou matrizes, e os ambientes vistos até agora não são suficientes para essa tarefa. Para alinhar itens verticalmente, criaremos uma espécie de tabela chamada `array`. Este é um ambiente que alinha colunas de acordo com a sua preferência. Veremos os 3 casos mais simples que são colunas alinhadas à esquerda (`l`), direita (`r`) ou centro (`c`).

Para começar um `array`, precisamos abrir e fechar o ambiente (`\begin{array}` e `\end{array}`). Porém só com essas informações ele não sabe quantas colunas deve fazer e nem qual é o alinhamento de cada uma. Para isso, escreveremos `l` `r` ou `c` para cada coluna (indicando seu alinhamento). 

Assim, para criar um array onde o primeiro item é alinhado à esquerda, o segundo é alinhado ao centro e o terceiro é alinhado à direita, podemos escrever:

```latex
\begin{array}{lcr}
\end{array}
```

Agora, vamos ao conteúdo. Para separar colunas usamos o símbolo `&` e para pular linhas usamos duas barras invertidas `\\`.

Veja o exemplo abaixo:

```latex
\documentclass{article}
\usepackage{amsmath}

\begin{document}

Neste exemplo, a primeira coluna é alinhada à direita, já a segunda coluna é alinhada à esquerda.
$$
\begin{array}{rl}
    4x -2x &= 10 -12 \\
    2x & = -2 \\
    x &=-1
\end{array}
$$

Neste outro exemplo, a primeira coluna é alinhada ao centro e a segunda coluna é alinhada à esquerda.
$$
f(x) = \left\{
\begin{array}{cl}
    x & \text{, se } x \leq 2 \\
    2x & \text{, caso contrário} \\
\end{array}
\right.
$$

\end{document}
```

![[Pasted image 20260723182029.png]]


> [!check] Próxima página
> [[Teoremas, Definições, etc.]]