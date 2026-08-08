---
title: 1.4 Imagens
draft: false
tags:
order:
---

Figuras são importantes para ilustrar documentos e em alguns casos a sua presença é imprescindível. Aqui, veremos de maneira simples, como inserir figuras. Inicialmente, é importante mencionar que o $\LaTeX$ não suporta nativamente a inserção de figuras. Para isso é necessário usar a biblioteca **graphicx**. Basta inserir no preâmbulo do seu documento o código `\usepackage{graphicx}`.

Para inserir uma figura no seu documento, primeiramente você deve adicioná-la aos seus arquivos do projeto no Overleaf. Na aba *File Tree*, basta clicar no botão `upload` e selecionar a sua imagem. Alternativamente, você pode simplesmente arrastar o arquivo da imagem para lá. 

![[Figuras/Pasted image 20260723184500.png]]

Feito isso, estamos prontos para inserir no documento. O comando para inserir a figura é `\includegraphics{NOME_DO_ARQUIVO}`. Na imagem acima, veja que o meu arquivo de imagem se chama `figura.jpg`, assim o meu código deve ser

 ```latex
 \documentclass{article}
 \usepackage{graphicx}
 
 \begin{document}
 
 \includegraphics{figura.jpg}
 
 \end{document}
 ```
 
 ![[Figuras/Pasted image 20260723185251.png]]

algumas figuras podem ser grandes demais e gerar um resultado estranho. No meu caso, a figura apareceu cortada. Você pode ajustar como a imagem aparece passando alguns parâmetros opcionais. Por exemplo, no meu caso, ajustar a largura para 10cm funcionou bem. Para isso escrevi `\includegraphics[width=10cm]{figura.jpg}`.

> Para que a imagem ocupe todo o espaço horizontal disponível, basta configurar `width=\textwidth`. Você também pode usar múltiplos como `width=0.5\textwidth` (50\% da largura do texto).

> [!tip] Dica
> Para organizar suas figuras com numeração, adicionar legendas e outros ajustes, consulte [[Figuras]].

> [!check] Próxima página
> [[Ambientes/index|Ambientes]]

