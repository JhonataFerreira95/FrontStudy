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

- A singla HTML significa `HyperText Markup Leguage` ou  linguagem de marcação de HyperText.

- É uma linguagem de marcação de texto usada para criar uma estrutura de elementos e suas informações, mais precisamente, os elementos de uma página web.

- Criada entre 1989 e 1990 para compartilhamento de pesquisas cietíficas entre Tim Bernes-Lee (físico inglês e autor da linguagem) e seus colegas de trabalho.

### Como funciona?

- Através de arquivos de texto com a extensão `.html`.

- Usando o que chamamos de `tag`, que representam os elementos que queremos exibir na página web.


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



- Títulos, parágrafos, listas, etc.

- Imagens, vídeos, áudios, etc.

- Formulários, caixas de texto, botões, etc.

- Divisores, cabeçalhos, rodapés, etc.



### Recomendações além da minha própria documentação

- Documentaçõa da [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML)!

- Documentação da [W3SCHOOLS](https://www.w3schools.com/html/html_intro.asp)!



## Estrutura de uma página web


- Uma página web é composta principais, o `head` e o `body`.

- A tag `head` define s meta dados do documento, ou seja, informações sbre o próprio documento.

- O `head` é feito para o navegador, para que ele "conheça melhor" a página HTML em questão.

- A tag `body` contém todo o conteúdo visível do documento.

- O `body` é feito para os usuários, ele é a página em si.



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

- **Utilze os formatos corretos como:**



    - JPEG:formato de mais qualidade, porém mais pesado.</li>

    - PNG:formato inferior ao JPEG, mas que pode ser comprimido mantendo a qualidade.

    - WEBP:formato criado especificamente para a web pelo Google, oferece o melhor equilibrio entre qualidade e tamanho.

    - SVG:formato usado para vetores, que são imagens geométricas super leves e que podem escalar para qualquer tamanho.


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

## Oganização da página com elementos genéricos, div e span

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
Para a navegação dentro da páginas usamos `href="#id_desejado"`, passamo no nosso atributo `href=""` o jogo da velha `#`, que representa a atribuição de um `id` dentro da página atual, lembrando que na hora de passar o `id` desejado, deve ser idêntico ao `ìd` que foi atribuido a sua tag.**

```html

<a href="#identificador">Link rápido </a> <!--Aqui usamos o `id` do exemplo acima-->

```
## Links externos

Bem, para utlizamos links externos na nossa página utlizamos um atributo `href=""`, porém temos que trata nossos links externos de forma absoluta e não de forma raltiva, caso trate de forma relativa isso ocasionará um erro. Irei utilizar como exemplo o site do Google, tbm utilizei o protocolo

```html

<p>Acessa a página do <a href="https:www.google.com">Google</a>.</p> <!--Aqui usei um link absoluto, já que o relativo aponta para um lugar dentro do seu domínio, então utlizamos o protocolo htpp(hypertext protocol), e como utilizei o `https` no lugar `htpp` já que o `https` é mais seguro-->

```

Um ótimo ponto para deixa a navegação salva para o usuário na sua página, é a utilização do atributo `target="_blank"`, é um atríbuto que abre uma nova página quando o usuário clicar no link externo, evitando perde a navegação atual.

```html

<p>Acessa a página do <a href="https:www.google.com">Google</a>.</p> <!--Além do `_blank` temos outros porém o mais padrão e nosso foco é nele-->

```

## Lista ordenadas e não ordenadas

Para utilização de uma lista ordenada númerica no `html` utilizamos a tag `<ol>`, as listas ordenadas são aquelas em que os itens são pontuados por numeração. Para criar uma lista ordenada usamos a tag `<ol>` e a tag `<li>` para reprensentar cada númeração da sua lista ordenada.

```html

<ol>
	<li>compras</li> <!--Isso no navegador ficará númerado-->
	<li>gastos</li>
	<li>promoções</li>
</ol>

```

Para utilização de lista não ordenada sem numeração no `html` utlizamos a tag `<uL>`, as lista não ordenadas são aquelas que possuí um carcacter de uma esfera totalmente preta ao lado, sem a presença de númeração, dentro da tag `<ul>` utilizamos as tag `<li>` também para criação de itens dentro da nossa lista.

```html

<ul>
	<li>compras</li> <!--Isso no navegador ficará com a esfera preta na frente do texto-->
	<li>gastos</li>
	<li>promoções</li>
</ul>

```

Lista ordenadas e não ordenadas de forma aninhada, é possível aninhar as nossas lista ordenadas e não ordenada.

```html

<h2>Bolos</h2>
    <ol>
        <li>
            <strong>Bolos Tradicionais</strong>
            <ol>
                <li>Bolo de Chocolate Fofinho</li>
                <li>Bolo de Cenoura com Cobertura de Chocolate</li>
                <li>Bolo de Limão com Glacê de Limão</li>
            </ol>
        </li>
        <li>
            <strong>Bolos de Festas</strong>
            <ol>
                <li>Bolo de Aniversário com Recheio de Frutas</li>
                <li>Bolo de Casamento com Flores de Açúcar</li>
                <li>Bolo de Natal com Frutas Cristalizadas</li>
            </ol>
        </li>
    </ol>

    <h2>Sobremesas</h2>
    <ul>
        <li>
            <strong>Sobremesas Geladas</strong>
            <ul>
                <li>Sorvete de Chocolate Caseiro</li>
                <li>Pudim de Leite Condensado</li>
                <li>Gelatina Colorida com Creme</li>
            </ul>
        </li>
        <li>
            <strong>Sobremesas Especiais</strong>
            <ul>
                <li>Mousse de Maracujá com Calda de Chocolate</li>
                <li>Cheesecake de Morango</li>
                <li>Pavê de Chocolate com Biscoitos</li>
            </ul>
        </li>
    </ul>

```

## Criação de tabelas no HTML

<ul>

- Bem, com as criações de tabelas não é algo tão bonito no `html` já que sua estrutura é super simples. 

- Para a criação de uma tabela no `html` utilizamos a tag `table`, dentro da nossa tag `table` existe um conjunto de tags para deixa a tabela mais organizada que são as tags: </li>


### `<tr>`

A tag `<tr>` é para gerar linha que no inglês significa `tables row` ou linha de tabelas na tradução.

```html

<table>

<tr> 

</tr>

</table>

```

### `<td>`

A tag `<td>` é um elemento da linha da tag `<tr>`, que em inglês significa `data cell in a table` ou calula com dados na tabela. Sendo assim, os dados dentro da linha.

```html

<table>

<tr> 

<td>dado 01</td>
<td>dado 02</td>

</tr>

</table>

```

### `<th>`

A tag `<th>` serve como célula do cabeçalho da tabela, por padrão a tag `<th>` fica em negrito para destaque que é cabeçalho da tabela. Para que a tag funciona é necessário está dentro da tag `tr` e posteriomente introduzir a tag `<th>`.

```html

<table>

<tr>

<th>Título</th>

</tr>

<tr> 

<td>dado 01</td>
<td>dado 02</td>

</tr>

</table>

```

### Tabelas com Cabeçalhos exemplos extras

Demonstrando tabelas com dados mais realistas

```html

<h2>Tabelas com Cabeçalho</h2>

<table>

<tr>

<th>nome</th>
<th>idade</th>
<th>profissão</th>

</tr>

<th>

<th>Bass</th>
<th>23</th>
<th>dev back-end</th>

</tr>

<th>

<th>Hisstrahr</th>
<th>20</th>
<th>dev front-end</th>

</tr>

</table>

```

### Separação da tabela do jeito morderno HTML 5

Nas versões mais recente do `html` podemos separar o cabeçalho da tabela do resto, isso fica em questão de acessebilidade com as tags `thead` para identificar o cabeçalho da tabela e `tbody` para o corpo dos dados na tabela, vou pegar o exemplo acima para fica mais claro. Além da acessebilidade, o código fica mais fácil de se ler e sua separação fica extramamente clara.

- **thread**

    ```html

    <h2>Tabelas com Cabeçalho</h2>

    <table>

        <thead> <!--Para a separação clara do cabeçalho-->

            <tr>

                <th>nome</th>
                <th>idade</th>
                <th>profissão</th>

            </tr>

        </thead>
        
        <tbody> <!--Para a separação clara dos dados da tabela-->

            <tr>

                <td>Bass</td>
                <td>23</td>
                <td>dev back-end</td>
                
            </tr>

            <tr>

                <td>Hisstrahr</td>
                <td>20</td>
                <td>dev front-end</td>

            </tr>
        
        </tbody>

    </table>

    ```

### Tabelas com Células Personalizadas e bordas

Aqui irei aborda o formatos nas células, como por dados que ocupam duas linha ou mais que isso até menos mesmo. 

```html

    <h2>Tabelas com células personalizadas</h2>
        <table>
            <thead>
            <tr>
                <th colspan="2">Informações Pessoais</th>
                <th>Contato</th>
            </tr>
            </thead>
            <tbody>
            <tr>
                <td>Nome:</td>
                <td>João</td>
                <td rowspan="2">Telefone: 123456</td>
            </tr>
            <tr>
                <td>Idade:</td>
                <td>30</td>
            </tr>
            </tbody>
        </table>

```
- colspan
    - Esse atributo serve para definir o tamanho que o seu dado vai ocupar na célula da coluna em seucabeçalho, para isso utilize a tag com a quantidade de tamanho que irá ocupar na coluna `colspan="2"`.

```html

    <thead>

        <tr>

            <th colspan="2">Informações Pessoais</th>
            <th>Contato</th>

        </tr>
    </thead>

```

- rowspan
    - Esse atributo serve para definir o tamanho que seu dado vai ocupar quantidade de linha na sua célula em sua tabela.

```html

    <tbody>

        <tr>

            <td>Nome:</td>
            <td>João</td>
            <td rowspan="2">Telefone: 123456</td>

        </tr>

        <tr>

            <td>Idade:</td>
            <td>30</td>

        </tr>

    </tbody>

```

- border
    - Esse atributo não é tão utlizado, porém é a borda para sua tabela diretamente com `html` sem o css. Para utilização do atributo `border="1"` para preencher a nossa tabela.

```html

    <h2>Tabelas com células personalizadas</h2>
        <table border="1">
            <thead>
            <tr>
                <th colspan="2">Informações Pessoais</th>
                <th>Contato</th>
            </tr>
            </thead>
            <tbody>
            <tr>
                <td>Nome:</td>
                <td>João</td>
                <td rowspan="2">Telefone: 123456</td>
            </tr>
            <tr>
                <td>Idade:</td>
                <td>30</td>
            </tr>
            </tbody>
        </table>

```

## Formulários no HTML

- O que são formulários?

    - Os formulários em `html` são estruturas que permitem a coleta de informações dos usuários, como nome, e-mail, senha, comentários, etc.

    - Eles são compostos por elementos `html` que possibiitam a criação de campos de entrada, botões e envio e outras funcionalidades.

    - Olando de forma simples, a comunicação na web ocorre de duas formas: Obtendo dados (como uma página ou uma imagem) e enviando dados. Os formulários são os principais responsáveis pela segunda.

    - Os formulário são compostos por

        - Uma tag `<form>` com os atributos `action` e `method`

        - Campos a serem preenchidos, como `<input>` ou `<select>`

        - Um botão para enviar, ou `submeter`, o formulários:

            - `<button type="submit">texto</button>`

### Exemplos de formulários

Práticando com a tag `<form>`, criei um formulários simples com um botão para demostrar o uso da tag `<form>` e `<button>`

```html

<body>

    <h1>Formulários no HTML</h1>

    <form action="http://google.com/search" method="get">
        <label for="pesquisar">pesquisar`no google</label>
        <input type="text" name"q">
        <button type="submit">Pesquisar</button>
    </form>
    
</body>

```

## Tipos de input no HTML

- Aqui irei aborda alguns tipos de `inputs` no `html`

    - Começando com um clássico botão de `submit` ou enviar, seu atríbuto é `type="submit"`, bem intuitivo.

    ```html

    <button type="submit">Enviar</button>

    ```

    - Temos o `input` campo de texto, seu atríbuto é `type="text"`, muito utilizado para coletar informações do usuário. Um pouco mais complexo, já que temos que atribuir um `id` para posteriomente utilizar em nossa `label` passa seu parâmetro no `for`, no caso do `name` é o atributo a ser enviado para autenticação no `back-end`, irei mencionar o `required` esse atríbuto obriga o usuário a preencher um campo, caso ele não seja preenchido ele não pode enviar. 

    ```html

    <input type="text" id="nome" name="nome" required>
    <label for="nome">Nome:</label>

    ```

    - Temos o `input` campo de email, seu atríbuto é `type="email"`, esse atríbuto só aceita email, deve conter um @ para ser considerado tipo email. Adicionamos um `id` para nosso atríbuto seja chamado em um `for` de uma `label` se for necessário, um `name` para chamada `back-end` e um `required` para o campo se torna obrigatório.

    ```html

    <input type="email" id="email" name="email" required>
    <label for="email">E-mail:</label>

    ```

    - Temos o `input` para campo de senha, seu atríbuto é `type="password"`, os valores com atríbuto de senha são ocultos para o usuário, é possível ver clicando no símbolo do olho no canto direito. Passei para nosso atríbuto `type="password"` um `id` para posteriomente passar em alguma `label` em seu `for` caso seja necessário, passei um `name` para chamada no `back-end` e um `required` para o campo se torna obrigatório. 

    ```html

    <input type="password" id="senha" name="senha" required>
    <label for="senha">Senha:</label>

    ```

    - Temos o `input` para campo de idade, seu atríbuto é `type="number"`, esse atríbuto aceita apenas números, já que seu campo é especifico para idade. Passei para nosso atríbuto `type="number"` um `id` para posteriomente passar em alguma `label` em seu `for` caso seja necessário, passei um `name` para chamada no `back-end` e um `min` para idade mínima do campo e `max` para idade máxima do campo.

    ```html

    <input type="number" id="idade" name="idade" min="18" max="120">
    <label for="idade">Idade:</label>

    ```

    - Temos o `input` para campo de marca/desmarca mais conhecido com `radio`, seu atríbuto é `type="radio"`, esse atríbuto tem opção de escolha, no exemplo utilizamos para seleção de sexo. Adicionei um `id` para nosso atríbuto `type="radio"` para que posteriormente passar em alguma `label` e em seu `for`, passei um `name` para chamada no `back-end` como passamos o mesmo `name` ambos atríbuto `type="radio"` vai ser o mesmo valor no `back-and`, então sendo uma opção de uma escolha. Adicionamos um atríbuto de `value` para o valor do `input` a ser enviado ao `back-end`.

    ```html

    <input type="radio" id="masculino" name="genero" value="masculino">
    <label for="masculino">Masculino</label>
    <input type="radio" id="feminino" name="genero" value="feminino">
    <label for="feminino">Feminino</label>
 
    ```

    - Temos o `input` para o campo de seleção múltipla escolha, seu
    atríbuto é `type="checkbox"`, com mencionamos antes, ele vai variar o seu `name` para chamada `back-end` ou seja, possibilitante várias ecolhas já que seu `name` será diferente. Adicionamos um `id` para utilizar posteriormente uma `label` e um `value` para ser um valor a ser enviado ao `back-end`, adicionei uma `label` com o `for` do atríbuto para cada um chamando os `id` respectivamente.

    ```html

    <input type="chackbox" id="frontend" name="frontend" value="frontend">
    <label for="frontend">Front-End</label>
    <input type="chackbox" id="backend" name="backend" value="backend">
    <label for="backend">Back-End</label>
    <input type="chackbox" id="mobile" name="mobile" value="mobile">
    <label for="mobile">Mobile</label>
    

    ```

    - Temos o `input` para o campo de data, seu atríbuto é `type="date"`, esse `input` aceita apenas o formato de data, ou seja dia/mês/ano. Adicionei um `id` para chamada no `for` na `label`, utilizei um `name` para chamada `back-end`.


    ```html

    <label for="dataNascimento">Data de Nascimento:</label>
    <input type="date" id="dataNascimento" name="dataNascimento">

    ```

    - Temos o `input` upload de arquivos, seu atríbuto é `type="file"`, essa atríbuto é feito únicamente para enviar qualquer tipo de arquivo(imagem/pfd/word/vídeo/etc), adicionei um `id` para utilizar no `for` de uma `label`, apliquei um `name` para chamada `back-end`.

    ```html

    <label for="fotoPerfil">Foto de Perfil:</label>
    <input type="file" id="fotoPerfil" name="fotoPerfil">

    ```

## Elementos Especiais no HTML

Creio que esses 2 input extra na minha opinião como acadêmico são importante, são eles `select`, `option` e `textarea`.

- Temos o elemento de `select` para o campo de caixa de seleções, o sua  tag é `<select name="" id="">texto</select>`, com alguns atríbutos padrão como `name` e `id`, já sabemos que o `id` é usado para passar em algum parâmentro para referência nosso `select`, no caso de exemplo foi a nossa `label`, e o `name` serve para chamada `back-end`.

    - Dentro da nosssa tag `select` temos a tag `option` para as opções dos campos a serem selecionado. A sua tag é `<option value="">texto</option>`, essa tag tem um atríbuto já conhecido, seu atríbuto é o `value` para que o valor da `option` seja enviado para o `back-end`. No exemplo, por default usei um `value=""` vázio com `disabled` para desabilitar a opção `selecione uma das opções` para que o usuário não possa selecionar essa opção, tbm adc um atríbuto de `selected` forçando o usuário a selecionar algo, assim fica mais intuitivo com o `selected disabled`.


```html

<label for="situacao">Situação Atual:</label>

    <select name="situacao" id="situacao">

        <option value="" selected disabled>Selecione uma das opções...</option>
        <option value="estudante">Estudando para me tornar um programador</option>
        <option value="estagiario">Atuando como estagiário/trainee</option>
        <option value="junior">Atuando como desenvolvedor júnior</option>
        <option value="pleno">Atuando como desenvolvedor pleno</option>
        <option value="senior">Atuando como desenvolvedor sênior</option>

    </select>

```

- Temos a elemento de `textarea`, sua tag é `<textarea></textarea>`na tag `<` ,juntamente com seus atríbuto `id=""` para identificação para passarmos para algum parâmetro, em nosso exemplo passamo em uma `label`, `name=""` para chamada no `back-end`, `cols=""` para quantidade de colunas na caixa de texto, `rows=""` para quantidade de linha em nossa caixa de texto e o `placeholder=""` uma descrição para o usuário saber para que serve a caixa de texto.

```html

<label for="sobre">Sobre Mim:</label>

<textarea name="sobre" id="sobre" cols="40" rows="6" placeholder="Fale um pouco sobre você..."></textarea>

```