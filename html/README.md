# Documentação sobre HTML5

## índices

00. [O que é HTML e como usá-lo](#o-que-é-o-html-e-como-usá-lo)
01. [Principais elementos e tags HTML](#estrutura-de-uma-página-web)
02. [Lista e tabelas]()
03. [Formulários e seus componentes]()
04. [Recursos do HTML 5]()
05. [Semântica e acessibilidade]()
06. [Boa prática e otimizações]()

## O que é o HTML e como usá-lo

#### O que é HTML?

A singla HTML significa `HyperText Markup Leguage` ou  linguagem de marcação de HyperText.

É uma linguagem de marcação de texto usada para criar uma estrutura de elementos e suas informações, mais precisamente, os elementos de uma página web.

Criada entre 1989 e 1990 para compartilhamento de pesquisas cietíficas entre Tim Bernes-Lee (físico inglês e autor da linguagem) e seus colegas de trabalho.

### Como funciona?

Através de arquivos de texto com a extensão `.html`.

Usando o que chamamos de `tag`, que representam os elementos que queremos exibir na página web.

Uma `tag` é algo como: 

```html

<p>isso é uma tag</p>

```

Uma `tag` pode ter atributos, que são características especiais de um determinado elemento.

Uma `tag` com um atrbuto é algo como: 

```html

<p id="paragráfo-principal"> isso é uma tag com atributo</p>

```

### Existem tipos de elementos HTML

Títulos, parágrafos, listas, etc.

Imagens, vídeos, áudios, etc.

Formulários, caixas de texto, botões, etc.

Divisores, cabeçalhos, rodapés, etc.

### Recomendações além da minha própria documentação

Documentaçõa da [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML)!

Documentação da [W3SCHOOLS](https://www.w3schools.com/html/html_intro.asp)!

## Estrutura de uma página web

Uma página web é composta principais, o `head` e o `body`.

A tag `head` define s meta dados do documento, ou seja, informações sbre o próprio documento.

O `head` é feito para o navegador, para que ele "conheça melhor" a página HTML em questão.

A tag `body` contém todo o conteúdo visível do documento.

O `body` é feito para os usuários, ele é a página em si.

### head

```html

<html>
<head>
	<title>HTML page</title>
</head>

</html>

```

### body

```bash

<body>
	<h1>Olá, mundo!</h1>
</body>

```

## Paragráfos e títulos

### Títulos

Começando pelos títulos, existem vários níveis de títulos e seguem uma ordem como `h1`, `h2`, `h3`... Vão até o `h6`, mais como é visto o `h1` é o maior título da página.

```html

<h1>Título 1: o título principal</h1> 

<h2>Título 2: o título secundário</h2> 

```

### Paragráfo

Bem, para textos simples e quebra de linha utilizamos a tag `<p>` que é refente ao paragráfo

```html

<p>Paragráfo</p>

```

## Elementos de formatação

No html podemos escreve utilizando negrito, ítalico ou abmos para destacar partes de um texto, isso com a tag `<b>texto</b>` para negrito ou `<i>texto</i>` para ítalico.

```html

<b>texto negrito</b>

<i>texto ítalico</i>

```

### Strong e Em

`<strong>` e `<em>` são novas tags do HTML 5 para substítuir as tags `<b>` e `<i>` para ser algo semântico, apesar de ambas ter o mesmo resultado.

```html

<strong>texto negrito</strong>

<em>texto ítalico</em>

```

## Comentários

Aqui serei breve, o uso de comentários não é muito utilizado, pois a grande maioria dos devs acham que deixam o código muito poluído, de qualquer forma, um comentário do html é feito assim

```html

<!--comentário-->

```

