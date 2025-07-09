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

Bem, para textos simples e quebra de linha utilizamos a tag `<p>` que é refente ao paragráfo, inclsuive quando você abre a tag `<p>` e fecha ela posteriomente, abre outra novamente, elas ficam separadas. 

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

## Atríbuto de imagem

Para acessar uma imagem no `html` usamo a tag `img` e dentro da tag `img` temos um atributo chamado `src` que signifca `source`, que sua tradução é `fonte`, ou seja, fonta de imagem.

```html

<img src="./caminho_da_imagem">

```

Também temos a presença do `alt`, que nada mais é do que um texto alternativo para imagem, caso a imageme esteja quebrada. Sem conta que entra na questão de acessibilidade.

```html

<img src="./caminho_da_imagem" alt="decrição">

```

## Alterar e largura no HTML 5

No html temos a presença de altura e largura da imagem, para complmentar isso, utilizerei o exemplo anterior. Os atríbutos são `height` para a altura e width` para a largura.

```html

<img src="./caminho_da_imagem" alt="decrição" height="100" width="50">

```

## Formatos e otimização de imagens

Importante saber que uma página web esteja sempre otimizada. Páginas pesada demoram para carregar gerando uma experiência ruim, consomem mais dados, que é ruim para quem tem dados limitados. Um dos aspectos que mais pode atrapalha uma página são suas imagens.

#

### Como otimizar as imagens?

Utilze os formatos corretos como: 

#### JPEG:formato de mais qualidade, porém mais pesado.
#### PNG:formato inferior ao JPEG, mas que pode ser comprimido mantendo a qualidade.
#### WEBP:formato criado especificamente para a web pelo Google, oferece o melhor equilibrio entre qualidade e tamanho.
#### SVG:formato usado para vetores, que são imagens geométricas super leves e que podem escalar para qualquer tamanho.

### Tamanhos corretos 

Imagens grande ficam pesada e pquenas demais ficam pixeladas, se necessários use o atríbuto `srcset` para definir diferente versões da imagem para diferentes dispositivos. Comprima a imagem, se possível.

## Quebra de linha e régua horizontal

Para pular linha no `html` usamos a tag `<br>` que se chama line break, por isso o nome `br`. Como visto anteriormente essa tag segue o mesmo padrão da tag `<img>`, que é uma tag auto-contida.

```html

<p>Exemplo de linha. <br> Exemplo de linha 2. <br> Exemplo de linha 3. </p>

```

A régua horizontal ou horizontal rule, é a função de régua horizontal utilizando a tag `hr` no html.

```html

<p>Exemplo de linha. <br> Exemplo de linha 2. <br> Exemplo de linha 3. </p>

<hr>

<p>quarta linha. <br> quinta linha. <br> sexta linha.</p>

```

## Oganização da página com elementos genéricos, <div> e <span>

No `html` possuímos 2 elementos genéricos para organização da página, para criar diferente divisões e blocos na nossa página esse elementos são o `<div>` e o `<span>`. A principal diferença entre esses dois é que o `<div>` organiza em blocos o conteúdo que ele agrupa e o `<span>` organiza os seus elementos em linha.

```html

<p> Um div é um grupo de código <div>que ocupa todo espaço horizontal disponível.</div> </P>  

```

Também no `html` temos a tag `<span>` que quebra linha ocupado apenas a largura do seu conteúdo interno

```html

<P>Exemplo <span>para o span</span></p> <!--Utilize o dev-tools no navegador para visualizar o <span>-->

```

## Trabalhando com links no HTML 

Irei aborda as tags de links ou âncoras no `html`. A tag que irei aborda agora é a tag `<a>`, ele funciona inline ou em linha na tradução, funciona de jeito parecido com o `<span>`. Sendo assim possível criar links dentro do texto. Bem, para que o link da tag `<a>` funcione precisamos de um atributo chaamdo `href="link_desejado"` que é a referência da url para onde você será direcionado, assim quando você adicionar o link entre as aspas, o tag `<a>` estará em funcionament com o link desejado.

```html 

<a href="www.outra_pagina.com.br">Vá para outra página</a>

```

## Url's absolutas ou relativas

O que é uma `url` absoluta? É um caminho completo de uma `url` de uma determinada página, enquanto uma `url` relativa ela não é um caminho completo e sim um caminho relativa a página atual. Uma `url` absoluta geralmente é atrelada a raiz da sua página/projeto.

### URL absoluta

```bash

http://localhost:5500/ # Aqui é um exemplo de URL absoluta

```

```html

<a href="/html/009_links_absolutos_relativos.html">Exemplo de outra url absoluta</a> <!--Aqui usei a raiz do projeto com "/" que representa a raiz para o exemplo-->

```

### URL relativa

```html

<a href="../html/009_links_absolutos_relativos.html">Exemplo de outra url relativa</a> <!--Aqui usei para começa na pasta atual "../" que representa a URL relativa para o exemplo, a diferença é clara, já que uma usa os "../" para relativa e a outra usa apenas "/" para absoluta-->

```

## Links dentro da página

No `html` existem link dentro da página, mais para esses links funcionar vamos falar sobre os atributos `id`, cada tag no `html` pode ter um atributo `id`, cabe você atribuir esse `id` a tag desejada. O papel do `id` é de identificar cada `tag` no html, e a ideia de `id` é que seja único, não se repete na mesma página. 

### id

```html

<div id="identifcador">exemplo de id</div> <!--Como pode ver, nosso atributo `id`, e podemo dar qualquer nome a esse `id`, no exemplo foi usado o "identificador", para algo mais didatico-->

```
Para a navegação dentro da páginas usamos `href="#id_desejado"`, passamo no nosso atributo `href=""` o jogo da velha `#`, que representa a atribuição de um `id` dentro da página atual, lembrando que na hora de passar o `id` desejado, deve ser idêntico ao `ìd` que foi atribuido a sua tag.

```html

<a href="#identificador">Link rápido </a> <!--Aqui usamos o `id` do exemplo acima-->

```
## Links externos

Bem, para utlizamos links externos na nossa página utlizamos um atributo `href=""`


