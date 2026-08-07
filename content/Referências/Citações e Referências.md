---
title: 3.1 Citações e Referências
draft: false
tags:
---
Em geral, todo o seu conteúdo de citação fica em um arquivo especial `.bib`. Nele, colocamos todas as informações sobre a fonte que estamos citando e as bibliotecas farão a formatação necessária, seja para normas ABNT ou outras. 

# A biblioteca 

O arquivo `.bib` pode conter artigos, livros, sites, etc. Cada uma dessas classes terão diferentes parâmetros como "autor", "url" ou "título".  Para criar uma biblioteca no seu projeto do Overleaf, basta clicar em `New file` dentro da *File tree* e dar um nome (não esqueça que o arquivo deve ter extensão `.bib`).

Aqui vai um exemplo de um arquivo `referenciass.bib` que contém um artigo e um livro.

```bib
@book{
	lamport1994, 
	author = {Leslie Lamport}, 
	title = {LaTeX: A Document Preparation System}, 
	publisher = {Addison-Wesley}, 
	year = {1994}, 
	address = {Reading, Massachusetts}, 
	edition = {2} 
} 

@article{
	silva2023, 
	author = {João da Silva and Maria Souza}, 
	title = {O uso de tecnologias na educação}, 
	journal = {Revista Brasileira de Educação}, 
	year = {2023}, 
	volume = {10}, 
	number = {2}, 
	pages = {15-30} 
}
```

A primeira linha dentro de cada objeto é o "label" da fonte, esse é o nome que usaremos no nosso documento quando quisermos fazer referência a ele. Evidentemente, não podemos usar o mesmo nome para diferentes fontes.

Este é um grande passo, mas não é tudo. É preciso indicar no documento `.tex` que estamos usando esse arquivo como referência. Além disso, é necessário um pacote adicional para processar essas informações. Para o nosso propósito, usaremos a biblioteca "abntex2cite" que já possui um cuidado especial com as normas ABNT. Assim, o nosso documento base terá a seguinte forma.

```latex
\documentclass{article}
\usepackage[alf]{abntex2cite}

\begin{document}
\bibliography{referencias}
\end{document}
```

O parâmetro `[alf]` indica que queremos exibir as referências em ordem alfabética. O comando `\bibliography{}` faz duas coisas: ele gera uma lista de todas as fontes que foram usadas no documento e ele também diz ao compilador qual é o nome do arquivo `.bib` onde estão as referências.

# Citando

No texto, existem duas formas principais de citar: 
- "Tecnologias favorecem a educação (Silva, 2023)."
- "De acordo com Silva (2023), tecnologias favorecem a educação."

Para o primeiro caso, usamos o comando `\cite{}`. Já no segundo caso, usamos `\citeonline{}`. Dentro das chaves, colocamos o "label" que ficou definido no nosso arquivo `.bib`. Abaixo, um exemplo completo usando o arquivo `referencias.bib` que definimos acima.


 ```latex
 \documentclass{article}
 \usepackage[alf]{abntex2cite}
 
 \begin{document}
 
 \LaTeX é um sistema computacional de editoração \cite{lamport1994}.
 
 De acordo com \citeonline{silva2023}, tecnologias favorecem a educação.
 
 \bibliography{referencias}
 \end{document}
 ```
 
 ![[Figuras/Pasted image 20260723220751.png]]

> [!check] Próxima página
> [[Referencias Cruzadas]]