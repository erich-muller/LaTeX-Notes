---
title: 1.1 Texto
draft: false
tags:
order:
---

A linguagem de marcação $\LaTeX$ tem os seus comandos para indicar quando um texto deve estar em negrito, quando começar uma seção e etc. Por esse motivo, é necessário uma certa ordem e organização lógica do código, bem como o uso correto de caracteres.

O $\LaTeX$ usa com frequência os seguintes caracteres para indicar comandos.
$$\backslash \quad \# \quad \$ \quad \% \quad \& \quad \_\quad  \{ \quad \}$$
Assim, devemos evitar usá-los de forma desnecessária. Para digitá-los no corpo do texto é necessário colocar uma barra invertida antes como em: `\\  \#  \$ \%  \&  \_ \{  \}`.

---
## Estilos de texto

Para um texto padrão, basta digitar entre o `\begin{document}` e o `\end{document}`. Todo o texto dentro dessa estrutura aparecerá no PDF final. Caso queira fazer alguma anotação no código, você pode usar o caractere `%` e todo o texto após ele será omitido. Vejamos a seguir alguns comandos básicos para editar estilos no nosso texto. 

Para deixar o texto em negrito, usamos o comando `\textbf{}`. Tudo que estiver entre as chaves ficará em negrito. Similarmente, os comandos `\textit{}` e `\underline{}` servem para deixar o texto em itálico e sublinhado, respectivamente. Veja o exemplo abaixo:

```latex
\documentclass{article}
\begin{document}

\textbf{Esse texto ficará em negrito.}

\textit{Esse texto ficará em itálico.}

\underline{Esse texto ficará sublinhado.}

\end{document}
```

![[Figuras/Pasted image 20260808145804.png]]


Para mudar o alinhamento do texto (centralizado, etc.) consulte 👉 [[Alinhamento]].

---
## Estilos de letras

Você pode ainda, caso necessário, usar outros comandos para customizar ainda mais as letras quanto ao tipo e tamanho. As tabelas abaixo demonstram o código necessário para cada ajuste.

![[Figuras/Pasted image 20260722154525.png | 450 ]]

![[Pasted image 20260722154545.png | 350]]


> [!todo]- Exercício
> Faça um documento $\LaTeX$ com o seguinte conteúdo e aparência:
> 
> ![[Pasted image 20260722155750.png]]

---

## Espaçamentos e quebras de linha.

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

> Para **quebrar uma página inteira** você pode usar o comando `\newpage`.

> [!check] Próxima página
> [[secoes subsecoes e outros | Seções, Subseções e outros]]

