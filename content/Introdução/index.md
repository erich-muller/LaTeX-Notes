---
title: 1. Introdução
draft: false
tags:
order:
---

O $\LaTeX$ é um sistema computacional de editoração para documentos científicos, livros e outras formas de publicação. Ele permite que os usuários formatem o documento, insiram equações matemáticas, figuras, tabelas, e vários outros elementos usando apenas texto e comandos *tagging* de marcação.

O sistema teve início em 1977 na Universidade de Stanford, onde Donald E. Kunuth, decepcionado pela baixa qualidade na editoração de materiais acadêmicos, decidiu criar um sistema computacional eficiente para editoração, hoje conhecido como $\TeX$.

Posteriormente, Leslie Lamport, com o intuito de permitir diagramação dos documentos científicos de qualidade profissional sem que necessite do conhecimento específico da editoração, iniciou um projeto para desenvolver macros (configurações) novos para o TeX. Tal projeto foi concluído em 1985 e recebeu o nome "LaTeX" (abreviação de Lamport TeX).

# Porquê usar $\LaTeX$?

O $\LaTeX$ se torna extremamente conveniente para documentos longos e/ou complexos. Na escrita de documentos acadêmicos e científicos, comumente é necessário ajustar número de figuras, tabelas, seções, capítulos e outros. Em programas como MS Word ou Google Docs, fazer esses ajustes manualmente é uma tarefa maçante, enquanto que no $\LaTeX$ esses ajustes são feitos automaticamente.

![[Pasted image 20260722140720.png]]

# Funcionamento

Um documento $\LaTeX$ é criado inicialmente a partir de um arquivo `.tex`. Nesse arquivo você escreve detalhadamente como quer o seu documento: formatação, conteúdo, etc. 

Para que possamos gerar um documento legível, precisamos passar o arquivo `.tex` por um compilador. O compilador é o responsável por ler o código e interpretar todas as instruções. Em suma, é ele quem converte o seu código `.tex` no que você vê no seu documento `.pdf`. 

|            Arquivo `.tex`             |               Arquivo `.pdf`               |
| :-----------------------------------: | :----------------------------------------: |
| `$\overline{x} = \sum^{n}_{i=1} x_i$` | $\overline{x} = \sum\limits^{n}_{i=1} x_i$ |

Após a compilação, se tudo correr bem, o compilador irá devolver o nosso arquivo `.pdf`. Caso o compilador encontre algum erro no código, ele irá exibir uma mensagem indicando onde está o erro.

![[Pasted image 20260722134241.png]] 
> https://pt.slideshare.net/slideshow/latex-introductionodashimafinal/66905048#2

Em geral, usamos ferramentas para facilitar a escrita e compilação de documentos $\LaTeX$. As ferramentas mais comuns são:

## Overleaf

O Overleaf é uma plataforma online que permite a criação de documentos LaTeX diretamente no navegador. Ele permite a escrita e compilação dos arquivos em nuvem. As suas principais características são:

- Permite o trabalho em grupo simultaneamente
- Backup automático de todo o seu documento
- Acesso a templates da comunidade
- Editor de texto com atalhos
- Tempo de compilação limitada em planos gratuitos
- Não precisa instalar nada

Sem dúvidas o Overleaf é uma das ferramentas mais usadas para criar documentos LaTeX. Entretanto a limitação do tempo de compilação pode ser um gargalo para quem precisa de documentos com muitas imagens.

## TeXstudio

O TeXstudio é um ambiente de escrita para documentos LaTeX offline e de código aberto. Assim como o Overleaf, permite a criação e compilação de documentos LaTeX com facilidade.

- Offline: não depende de internet
- Requer a instalação dele e de outros componentes base (como o mikTeX)
- Compilação ilimitada
- Tempo de compilação depende da sua máquina


Iremos nos concentrar no Overleaf para este minicurso.


---
# Primeiros passos

Acesse http://overleaf.com e crie sua conta (ou faça login com Google/ORCID).

Agora vamos criar o nosso primeiro projeto! Após ser redirecionado para a página de projetos, clique em `New Project > Blank project`. Dê um nome ao seu projeto e clique em `Create`. Após o carregamento você verá uma tela como essa:

![[Pasted image 20260722144510.png]]

## A interface

Podemos dividir a interface do site em 3 colunas: 
- **File tree**: é onde ficam os arquivos (o arquivo base `main.tex`, figuras e etc.)
- **Editor**: é onde podemos visualizar os arquivos e modificá-los. É nele que iremos escrever todo o nosso código $\LaTeX$.
- **Preview**: é onde vemos o PDF que foi gerado pelo compilador. 

Sempre que mudarmos o nosso código, precisamos recompilar para ver o resultado da modificação. Para isso, basta clicar no botão `Recompile` em verde.

Como é possível observar, o Overleaf já criou um código base no nosso documento. Vamos descartá-lo e começar do zero.

## Documento Básico

Todo o documento `.tex` é composto de 2 partes: preâmbulo e texto.

O preâmbulo é a primeira parte do documento. Nessa parte fica definido o tipo de documento, pacotes a serem usados e outras configurações iniciais, nada do que fica escrito aqui é passado diretamente para o PDF. Já a parte do texto é o restante do documento (que ficará visível no arquivo final). O texto sempre começa com `\begin{document}` e termina com `\end{document}`.

Um documento básico pode ser escrito como:

```latex
\documentclass{article}

\begin{document}
Olá, esse é o meu documento.
\end{document}
```

Nesse exemplo, o preâmbulo contém apenas o tipo de documento (artigo). O comando `\documentclass{}` diz ao compilador o que estamos escrevendo. Dependendo do tipo de arquivo, teremos uma formatação completamente diferente. Por exemplo: `\documentclass{book}` diz que estamos escrevendo um livro e fará paginação por capítulos; já o `\documentclass{beamer}` diz que estamos escrevendo uma apresentação e organizará o documento em slides. 

> [!bug] Cuidado
> Diferentes tipos de arquivos possuem diferentes conjuntos de comandos. Alguns comandos só funcionam em *article*, outros só em *beamer*, etc.



> [!check] Próxima página
> [[Texto]]




