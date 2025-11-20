# Documentação sobre CSS3

## índices

00. [O que é o CSS3 e como usá-lo](#documentação-sobre-css3)
01. [Cores e estilos básicos](#corres-e-estilos-básicos)
02. [DevTools](#devtools)
03. [Cores](#cores)
04. [Background e Border](#background-e-border)
05. [Margin e Padding](#box-model-margin-e-padding)
06. [Displays Básicos](#display-none-inline-block-e-inline-block)
07. [Seletores Básicos](#seletores-básicos)

## O que é o HTML e como usá-lo

#### O que é CSS?

- A sigla `css` significa `Cascading Styles Sheets` ou folhas de estilo em cascata.

- A linaguagem é usada para definir os estilos em um documento `html

- Pode ser incluido no documento de 3 modos:

    - Utilizando o atríbuto style, por exemplo:

        ```css

            <h1 style="color: red;">Título Vermelho</h1>
        
        ```

        - Aqui utilizamos a elemento `h1` com a junção do atríbuto de `style="color"` para definição de uma cor ao nosso título.

    - Com a elemento `style`, por exemplo:

        ```css

            <head>
                <style>h1 {
                    color:red;
                }</style>
            </head>

            <body>
                <h1>Título vermelho</h1>
            </body>

        ```

        - Com a elemento `style`, podemos aplicar regras de `css` diretamente dentro do documento `html`, sem precisar de um arquivo externo. Ela deve ser colocada dentro da elemento `head`, que é responsável por conter as informações de configuração e estilo da página.

    - Utilizando a elemento link apontando para um arquivo `css` que é o mais comum, por exemplo:

        ```css

            <link rel="stylesheet" href="style.css">

        ```

        - Adicionamos a elemento `link` para linkar ao nosso `html` e apontamos para o nosso arquivo css com o atríbuto `href=""`, e o atríbuto `rel=stylesheet` informa ao navegador que é uma folha de estilo `css`.

- Estrutura de um código em `css` usando como exemplo um o código:

    ```css

        h1{color: red;}

    ```

    - `h1` é o seletor, ou seja, o termo que seleciona qual parte do documento terá estilo.

    - As chaves `{}` delimitam o bloco de declarações, ou seja, onde começam e terminam os estilos a serem aplicanos no(s) elemento(s) selecionado(s).

    - A declaração `color:red;` define um estilo. Declaração são sempre compostas por duas partes, a `proriedade` e o `valor`, separadas por vírgula, e finalizadas por um ponto e vírgula.

        - Exemplo:

            ```css

                seletor{
                    proriedade: valor;
                    outra-proriedade: valor;
                }

            ```

## Corres e estilos básicos

- Como foi visto ateriormente, existem 2 formas de utilizar o `css` no `html`

    - 1 Utilizando via a elemento `link`
    - 2 Utilizando via atríbuto `style`

- A forma mais comum é criando um arquivo serpado para utiização do código `css` atráves da elemento `link` apontando para o mesmo.

    - Exemplo:

        ```css

            <link rel="stylesheet" href="../001_comeco.css"> <!-- Linkando o ccs por link no arquivo-->
        
        ```
    
    - Utilizando o atríbuto `href=""` para apontar ao destino do arquivo `css` de forma absoluta.

### Cores diretamente no arquivo `css`

- Vale ressaltar que o `css` é em castaca, então a última propriedade definida para determinada elemento vai ser a alterada.

    - Exemplo na prática:

        ```cs 

            p{
                color: white;
            }

            p{
                color: blue;
            }

            p{
                color: red;
            }
        
        ```

    - Resultado:

        - Aqui a cor definida é a cor `red`, já que ela é a última a ser definida, como é em forma de cascata a última sempre será a definida, é um padrão no `css`.

### DevTools

- Irei aborda agora sobre nossa ferramente de desenvolvedor ou `DevTools`.

- Utilizando o `DevTools` podemos mudar o estilo da página e os seus elementos porém de forma temporária, para isso normalmente visualizamos isso na aba do `DevTools` em `Elements` e `Styles`.

    - Exemplo na prática:

        ![DevTools](../css/assets/imagens/DevTools.png)

- Posso altera isso de forma temporária, basta selecionar a elemento desejada no `Elements` e alterar o estilo dela no `Styles`, para alterar o `html` é no `Elements` e no `css` no `Estyles`.

    - Exemplo na prática `Elements`:

        ![Elements](../css/assets/imagens/ElementsTagP.png)

    - Exemplo na prática `Styles`:

        ![Styles](../css/assets/imagens/StylesTagP.png)

    - Resultado:

        - Como já foi mencionado, toda manipulação feita aqui é reversível a partir do momento que você atualiza a página.

- Também podemos ver todas as própriedade que estão sendo aplicadas em nosso `css` através do `computed`.

    - Exemplo na prática:

        ![Computed](../css/assets/imagens/Computed.png)

    - Resultado:

        - Observa-se que selecionamos novamente a elemento `p` e ali temos todas as suas propriedades e seu tamanho.

        - margin, border, padding

            ![marginbordepadding](../css/assets/imagens/MarginBorderPadding.png)

        - margin:

            - Todas as elementos possuem `margin`, que nada mais é que o espaçamento entre as laterais, superior e inferior ao elemento.

        - border:

            - A propriedade `border` define uma borda ao redor de um elemento `html`. 
        
        - padding: 

            - O `padding` é o espaço interno entre o conteúdo de um elemento e sua borda.

        - With e hight:

            - Nada mais é que a altura x largura, representada pelo block azul no centro por `Largura-->452x18<--Altura`.

## Cores

- No `css` podemos trabalhar com cores em vários formatos:

- Usando nome de cores.

    - Podemos utilizar cores no `css` referênciando pelos nomes.

    - Exemplo na prática:

        ```css

            h1 {color: red;}
        
        ```
    
    - Não recomendo, pois não há uma garantia de pradronização das cores, por quê? Por que você trabalha com nome de cores no `css` ele vai utlizar a definição do navegador para a cor que foi determinada pelo nome, que no exemplo foi o `red`.

- Usando os código das cores
    
   - Forma recomendada, pois é específica a cor exata a ser usada de forma precisa.

    - Códigos RGB:

        - Utiliza  a função `rgb()` do `css` para processar uma cor a partir dos valores `red`, `green` e `blue` == `rgb`.

        - Exemplo na prática:

            ```css

                h1{color: rgb(255, 0, 0);}

            ```

        - Resultado:

            - Vale resltar que os números presentes no `rgb` vão do 0 ao 255, e cada valr definido dentro do `rgb`, vai ser o equilibrio de cada cor, em nosso exemplo temos `255, 0, 0`, sendo `255=red` a tonalidade máxima de vermelho, `0=green` a tonalidade zerada de verde e `0=blue` a tonalidade zerada de azul.  

    - Códigos hexadecimais:

        - Utiliza a numeração hexadecimal para especificar cores em formato `rgb` de forma abreviada.

        - O formato usado é o `#RRGGBB`, e os valores são convertidos de hexadecimal para decimal.

        - Números hexadecimais representam os valores decimais de 0 a 15, porém os algarismo `0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E e F`.

        - Exemplo na prática:

            ```css

                h1{color: #FF0000;}
            
            ```
        
        - Resultado:
        
           - Onde: `FF=255, 00=0 e 00=0`

    - Códigos HLS:

        - Formato diferente, porém muitoútil para manipulação de cores.

        - Utiliza o esquema de `tonalidade`, `saturação` e `brilho`, ou `Hue`, `Saturation` e `Lightness`, para definir uma cor.

        - Assim como no `rgb`, o `css` também possui uma função `hsl()` 

        - Exemplo na prática:

            ```css

                h1{color: hsl(0, 100%, 50%);}
                
            ```
        - Resultado:

            - Aqui no exempo usamos mais a `satuaração em 100%`, `50% no brilho` e `0% na tonalidade`.

## Background e Border

- Aqui irei aborda um pouco sobre a propriedade no `css` chamada `background` no primeiro momento, em seguida irei da uma atenção a propriedade `border`.

- Background:

    - A propriedade `background` é um atalho para definir valores de fundo individuais em um único lugar na folha de estilo.

    - Exemplo na prática:

        ```css

            header {
                background-color: #000;
                color: #ffffff;
            }

        ```

    - Resultado:

        - Sabemos que o `color` muda a cor dos nomes, enquanto o `background` muda o background de fundo de uma elemento definida. Vale resltar que o `backgroud` funciona tanto com elementos `html` quando com atríbutos, só que com atríbutos só irá funciona caso seja definido um `id` para o atríbuto desejado.

    - Trabalhando com `backgroud` e função `rgb`:

        - Podemos definir um padrão de `red`, `gree` e `blue` no nosso `background`, fica a seu critério.

        - Exemplo na prática:

            ```css
                    
            body{
                background-color: rgb(61, 61, 203);
            }

            ```

    - Trabalhando com `background` e função `url` para imagens.

        - Podemo também utilizar o `background` com imagem por link ou caminho relativo ou absoluto.

        - Exemplo na prática:

            ```css

                body{
                    background-image: url("https://codetheweb.blog/assets/img/posts/css-advanced-background-images/cover.jpg");
                    background-size: cover;
                }

                ```
        
        - Resultado:

            - Aqui utilizamos o `background-image` para definir que utilizariamos uma imagem como `background` porém o `css` não entende se apenas colocamos o link da imagem em `strig`, é necessário utilizar a função `url()` e depois abrir uma `strig` e por o link da imagem lá para que funcione.

            - Também utilizamos a propriedade `background-size` para definição do tamanho da imagem de fundo e a função `cover` que é para cobri todo o fundo da página.

- Border

    - A propriedade `border` é utilizada para definir a borda de um elemento(elemento ou atríbutos com `id`) no `html`, geralmente utilizada para aplicar no elemento para ter as suas características alteradas como o seu tamanho, a sua cor ou seu estilo.

    - Propriedades do `border`

        - Começando com o `border-width` que é a largura da borda.

        - Também temos o `borde-color` para definir a cor da nossa borda.

        - E para que a nossas propriedade `border` funcione precisamos adicionar o tipo de borda que vamos ter, aqui irei utilizar o `borde-style` com a função `solid`.

        - Resultado:

            ```css

                main {
                    background: #e5e5e5;
                    border-width: 4px;
                    border-color: #1c1a1d;
                    border-style: solid;
                }

            ```
        
        - Existem vários tipo de borda, aqui citei só um exemplo, fica a vontade para ir ao `MDN` para pesquisa sobre mais bordas ou no próprio `vscode` é possível ver várias.

- Estilizando uma `div` com `class=""`

    - Aqui irei passar a estilizar um `div` com atríbuto `class` bem rápido.

    - Exemplo:

        ```css

            .box1{
                background-color: #169436;
                border: 4px solid #1c1a1d;
                height: 64px;
                width: 320px;
            }

        ```

    - Resultado:

        - Aqui utilizamos o `.box` para referência uma `class` no `htlm`, utilizamos o `background-color` para definir o fundo, usei a própriedade `border` para definir o tamanho da borda que é `4px` o tipo que é `solid` e sua cor que é `#1c1a1d`, definimos sua altura com `height` e sua largura com `width`.

    - Aqui irei estililizar outra `div` com atríbuto `class`.

    - Exemplo: 

        ```css

            .box2{
            background-image: linear-gradient(to left, #2c2c2c, #f64348);
            height: 64px;
            width: 320px;
        }

        ```

    - Resultado:

        - Aqui utilizamos o `.box` para referência uma `class` no `htlm`, utilizamos o `background-image` para definir o tipo de fundo e `linear-gradient` para definir que o o fundo seja gradiente, utilizei o `linear-gradient(to left, #2c2c2c, #f64348` definindo o gradiente da esquerda para direito e suas cores que foi `#2c2c2c` e `#f64348`, após definir o tamanho de altura e largura que foi ` height: 64px` e `width: 320px`.

    
    - Aqui irei estilizar outra `div` com atríbuto `class`.

    - Exemplo:

        ```css

            .box3{
                background-color: #0077ff;
                border: 2px solid #1c1a1d;
                border-radius: 5px;
                height: 64px;
                width: 320px;
            }

        ```

    - Resultado:

        - - Aqui utilizamos o `.box` para referência uma `class` no `htlm`, utilizamos o `background-color` para definir o fundo, usei a própriedade `border` para definir o tamanho da borda que é `2px` o tipo que é `solid` e sua cor que é `#1c1a1d`, e para deixamos a borda arendondada utilizamos a propriedade `border-radius` com o pixel em 5 `5px` após isso definimos o tamanho de largura e altura que foi `height: 64px;` e `width: 320px;`.

# Box model: margin e padding

- Aqui irei aborda sobre o `box model`, afinal as páginas webs utilizam o modelo de caixa, por isso o nome `box model`, quando se criar uma página `html` ou qualquer coisa web, eles seguem o modelo de caixa.

- Margin: 

    - Todo espaço em volta do elemento é a `margin`, já falei um pouco da `margin` aqui no [DevTools.](#devtools)

    - Exemplo de `margin` na prática:

        ```css

            .box{
                margin-top: 30px; /* margin do topo da página*/
                margin-right: 40px; /* margin do direita da página*/
                margin-left: 40px; /* margin do esquerda da página*/
                margin-bottom: 30px; /* margin da parte inferior da página*/
            }

        ```
    
    - Resultado:

        - Aqui utilizei o `margin-top` para definir um espaçamento entre o topo e o nosso elemento, utilizei o `margin-right` para definir o espaçamento da direita, `margin-left` para definir o espaçamento da esquerda e o `margin-bottom` definir o canto infeior do nosso elemento.

    - Exemplos no DevTools:

        ![espacamento](../css/assets/imagens/espacamento.png)

        - Como pode ver as propriedades aplicada do `margin` e seu espaçamento ao redor do elemento.

        ![espacamento2](../css/assets/imagens/espacamento2.png)

        - Como ver é o `DevTools` e a parte em laranja é nossa `margin`, fica marcado o espaçamento que definimos.

- Padding:

    - Todo elemento tem um preenchemento que é o `padding` ele faz o espaço dentro do elemento, já falei um pouco do `padding` aqui no [DevTools.](#devtools)

    - Exemplo de `padding` na prática:

        ```css

            .box{
                padding-top: 10px;
                padding-right: 20px;
                padding-left: 20px;
                padding-bottom: 10px;
            }

        ```

    - Resultado:

        - Aqui utilizei o `padding-top` para definir o espaçamento no canto superior do elemento, utilizei o `margin-padding-right` para definir o espaçamento do elemento para direito, `padding-left` para definir o espaçamento para esquerda e `padding-bottom` para espaçamento no canto inferior do elemento.

    - Exemplos no DevTools:

        ![paddingespacamento](../css/assets/imagens/padding.png)

        - Como pode ver as propriedades aplicada do `padding` em seu espaçamento dentro do elemento.

        ![paddingespacamento2](../css/assets/imagens/padding2.png)

        - Como ver é o `DevTools` e a parte em verde é o nossa `padding`, fica marcado o espaçamento que definimos.

## Display: none, inline, block e inline-block

- Hoje irei aborda as propriedades `display: none`, `inline`, `block` e `inline-block`, existem vários tipos de displays além desses 4 apresentados, só que são os padrões pelos navegadores, além de serem os mais simples.

- `Display: inline`

    - Utilização do `inline` não quebra de linha, largura mínima, apenas aceita margem e preenchimento horizontal.

    - Ocupa apenas o espaço do conteúdo.

    - Fica na mesma linha (não quebra linha).

    - Ignora width e height.

    - `margin/padding` vertical não empurra outros elementos.

    - Exemplo na prática:

        ```css

            .inline{
                margin-top: 10px;       /* ❌ não funciona */
                margin-bottom: 10px;    /* ❌ não funciona */
                margin-left: 20px;      /* ✅ funciona */
                margin-right: 20px;     /* ✅ funciona */
                padding-top: 10px;      /* ⚠️ funciona parcialmente (não empurra outros elementos) */
                padding-bottom: 10px;   /* ⚠️ funciona parcialmente */
                padding-left: 20px;     /* ✅ funciona */
                padding-right: 20px;    /* ✅ funciona */
                width: 200px;           /* ❌ não funciona */
                height: 100px;          /* ❌ não funciona */
            }

        ```

    - Resultado: 

        ![inline](../css/assets/imagens/display_inline.png)

        - Como já foi mencionado, o `inline` não aceita propriedade vertica, ou seja, `top` e `bottom`, aceita apenas na horizontal como `left` e `right`.

- `Display: block`

    - Utilização do `block` quebra de linha, largura máxima, aceita margem e preenchimento vertical

    - Ocupa toda a largura do container

    - Quebra linha antes e depois

    - Aceita width e height

    - Margin e padding funcionam normalmente

    - Exemplo na prática:

        ```css

            .block{
                margin-top: 10px;       /* ✅ aceita */
                margin-bottom: 10px;    /* ✅ aceita */
                margin-left: 20px;      /* ✅ aceita */
                margin-right: 20px;     /* ✅ aceita */
                padding-top: 10px;      /* ✅ aceita */
                padding-bottom: 10px;   /* ✅ aceita */
                padding-left: 20px;     /* ✅ aceita */
                padding-right: 20px;    /* ✅ aceita */
                width: 200px;           /* ✅ aceita */
                height: 100px;          /* ✅ aceita */
            }

        ```

    - Resultado: 

        ![block](../css/assets/imagens/display_block.png)

        - No `block` aceitamos quebra de linha e todo tipo de propriedade, e sua margem é vertical além de definimos o widht e height se quisermos.

- `Display: inline-block`

    - Utilização do `inline-block` não quebra linha.

    - Fica na mesma linha como inline

    - Aceita width e height como block

    - Margin e padding funcionam completamente

    - Exemplo na prática:

        ```css

            .inline-block{
                display: inline-block;
                margin-top: 10px;       /* ✅ aceita */
                margin-bottom: 10px;    /* ✅ aceita */
                margin-left: 20px;      /* ✅ aceita */
                margin-right: 20px;     /* ✅ aceita */
                padding-top: 10px;      /* ✅ aceita */
                padding-bottom: 10px;   /* ✅ aceita */
                padding-left: 20px;     /* ✅ aceita */
                padding-right: 20px;    /* ✅ aceita */
                width: 200px;           /* ✅ aceita */
                height: 100px;          /* ✅ aceita */
            }

        ```

    - Resultado: 

        ![inline-block](../css/assets/imagens/display_inline_block.png)

        - O display `inline-block` não quebra de linha mas permite o preenchimento vertical e horizontal como `margin-top/margin/bottom` e `padding-top/padding/bottom`.

- `Display: none`

    - Utilização do `none`apenas esconde os elementos

    - Remove completamente o elemento do layout

    - Não é renderizado nem ocupa espaço

    - Fica invisível e ignorado pelo navegador

    - Exemplo na prática:

        ```css

           .none{
                display: none;
                margin-top: 10px;       /* ❌ ignorado */
                margin-bottom: 10px;    /* ❌ ignorado */
                margin-left: 20px;      /* ❌ ignorado */
                margin-right: 20px;     /* ❌ ignorado */
                padding-top: 10px;      /* ❌ ignorado */
                padding-bottom: 10px;   /* ❌ ignorado */
                padding-left: 20px;     /* ❌ ignorado */
                padding-right: 20px;    /* ❌ ignorado */
                width: 200px;           /* ❌ ignorado */
                height: 100px;          /* ❌ ignorado */
            }

        ```

    - Resultado: 

        ![none](../css/assets/imagens/display_none.png)

        - O `none` não tem alteração visual no navegador, ou seja, tudo é ignorado.

## Seletores Básicos

- O que são seletores?

    - São um padrões usados para selecionar elementos no `html` específicos para que possam ser estilizados. Eles determinam quais elementos de um documento `html` receberão uma regra de estilo definidas no `css`, e os tipos mais comuns incluem seletores de `class` e `id`, que são seletores básicos, nosso foco serão estes.

    - Seletor universal:

        - O seletor universal nos permite aplicar os estilos em todos os elementos `html`. A representação do seletor universal no `css` é o `*`, o porque utilizar o estilo universal? Para a normalização do estilo no navegador.

        - Exemplo na prática:

            ```css

                *{
                    margin: 0;
                    padding: 0;
                }

            ```
        - Resultado:

            - O seltor universal é utilizado para aplicar estilos em tudo como o próprio nome já diz e também é possíve remover tudo, até mesmo os estilo padrões do navegadores, assim permitindo que nossa estilização seja criada do absoluto zero.

    - Seletor de elemento:

        - O seletor de elemento permite que possamos pegar uma elemento e estilizamos apenas aquele elemento com a elemento específica.

        - Exemplo na prática:

            ```css

                header, footer{
                    background-color: #333;
                    color: #fff;
                    padding: 10px;
                }

            ```

        - Resultado:

            - Aqui estamos utilizando o seletor de elemento, como pode ver, aplicamos diretamento os estilos utilizando as elementos `html`, podemos aplicar o mesmo estilos para várias elementos apenas utilizando a vírgulas para separá-las 

    - Seletor de Elementos aninhados:

        - Seletor de elementos aninhados nada mais é que uma seleção de uma elemento que está dentro de outro elemento, não precisamos separar os elementos por vírgula quando o seletor é aninhados.

        - Exemplo na prática:

            ```css

                nav a {
                    color: #27ae60;
                }

            ```

        - Resultado:

            - Como pode ser visto, estamos utilizando o seletor de elementos aninhados, afinal estamos acessando a elemento `nav` e posteriomente nossas elementos `a` para estilização, por isso é chamado de aninhados, já que acessamos elementos dentro de outro elemento.

    - Seletor de Filhos:

        - O seletor de filhos são aqueles elementos dentro de outro elemento, podemos estilizar o elementos em específico, diferente do seletor aninhado.

        - Exemplo na prática:

            ```css

            nav > a {
                display: block;
                color: #f5a623;
                padding: 10px;
            }

            ```

        - Resultado:

            - Nota-se que, o seletor de filho estilizar apenas o elemento que está dentro de outro elemento, utilizando o sinal maior que `>` e o elemento desejado, aqui pegamos o filho do elemento `nav`, que era um `a` e adicionamos um `block`, `color` e `padding`, observa-se que apenas ele mudou, já que os outros elementos `a` são filhos da elemento `li`.

    - Seletores de Classes

        - Esse é o mais utilizado, podemos ir em nossa `html` e pegar-mos a `class` desejado e estilizar com a nomeclatura `.<node_da_class>`, assim comecariamos a estilizar uma `class`.

        - Exemplo na prática:

            ```css
            
            .laranja{
                color: #f5a623
            }

            .verde{
                color: #27ae60 
            }  

            ```

        - Resultado:

            - Aqui utlizamos o seletor de `class` para estilizar as classes atribuídas como laranja e verde.

    - Seletores de Id

        - Os seletores de `id` quando atribuímos um `id` a um elemento `html`, estilizamos eles a partir do seu `id` no `css`, a nomeclatura utilizada para estilizar um `id` é a seguinte `#<nome_do_id_no_html>`.

        - Exemplo na prática:

            ```css

                #secao-principal{
                    padding: 20px;
                    text-align: center;
                }

            ```

        - Resultado:

            - Utilizamos o `id` para estilizar o elemento `section` em específico, centralizamos todo o texto com um `text-aling: center;` e uma borda com `padding: 20;`.
    
    - Combinação de seletores

        - Podemos fazer a combinação de N seletores.

        - Exemplo na prática:

            ```css

                #secao-principal > * {
                    margin-top: 10px;
                }
            
            ```

        - Resultado:

            - Aqui estamos combinando os seletores `id` com o `*` universsal, juntamos os dois com o símbolos maior que `>` e todos os elementos da seção príncipal ficou com um espaçamento de `10px`.

    - Seletor de Sequência

        - Utilizam combinadores para estilizar elementos com base em sua posição relativa ou na sequência em que aparecem no documento `html`.

        - Exemplo na prática:

            ```css

                input + input{
                    margin-top: 30px;
                    margin-bottom: 30px;
                }

            ```

        - Resultado:

            - Aplicamos o seletor de sequência no nosso `ìnput`, pegamos o primeiro `input` que aplicamos e funciona assim, ele vai estilizar o elemento do segundo`input` mas nunca o primeiro.

    - Seletor de Atríbuto

        - Esse é um dos seletores mais simples de se utilizar, já que iremos pegar como base o atríbuto atribuído lá no `html` a um elemento.

        - Exemplo na prática:

            ```css

                input[name="email"]{
                    background-color: orange;
                }

                input[type="password"]{
                    background-color: green;
                }

            ```

        - Resultado:

            - Aqui estamos estilizanos os input pelos seus atríbutos `name` e `type`, é simples já que se atualizamos um o outro fica exatamente como está, sem alteração nenhuma, já que estamos estilizando ele por seu atríbuto.

## Textos e Fontes

- Para utilizamos apenas o `html` para criar o esqueleto do nosso site, as fontes e os textos podem ser passadas ou moldadas diretamente em nosso arquivo `css`.

    - `texts`:

        - `text-align`:

            - O `text-align` serve para definir o alinhamento horizontal(esquerda ou direita), vertical(cima ou baixo) o texto de uma `tag`, `seletor`, `classe` ou `id` específico.

            - Exemplos:

                ```css

                    header {
                    text-align: center;
                    }

                ```

            - Resultado:

                - Aqui utilizamos o `text-align: center;` para centralizamos o nosso texto no centro com a propriedade `center`.

        - `text-decoration`:

            - O `text-decoration` serve para decorar o nosso texto com nosso seletores como `tag`, `class`, `id` ou `tag`.

            - Exemplos:

                ```css

                    header {
                        text-decoration: underline;
                    }

                ```

            - Resultado:

                - Aqui utilizamos o `text-decoration: underline;` para decorar o nosso texto de uma forma que ele fique sublinhado.

        - `text-tranform`:

            - O `text-tranform` permite modificar os nossos textos para maiúsculo ou minúsculo, `upecase` ou `downcase`.

            - Exemplos:

                ```css

                    header {
                        text-transform: lowercase;
                    }

                ```
            
            - Resultado:

                - Aqui utilizamos o `text-transform: lowercase;` para deixa todas as letras minúsculas.

    -  `Fonts`:

        - `font-family`:
        
            - O `font-family` permite modificar o estilo da font no `html` diratemente no `css`.

            - Exemplos:

                ```css

                    h1 {
                        font-family: cursive;
                    }

                ```

            - Resultado:

                - Aqui utiizamos `font-family: cursive;` para estilizar o estilo de uma fonte no `html` usando o `css`.

        - `font-weight`:

            - O `font-weight` é utilizada para definir o contraste da fonte, se você quer que a fonte fique mais fina ou mais robusta via `css`.

            - Exemplos:

                ```css

                    h1 {
                    font-family: cursive;
                    font-weight: 100;
                    }

                ```

            - Resultado:

                - Aqui utilizamos o `font-weight: 100;` para deixar a fonte com um constraste mais grosso em nossa `font-family: cursive;`.

        - `font-size`:

            - O `font-size` é utilizado para definir o tamanho da fonto no `html` via `css`.

            - Exemplos: 

                ```css

                    h2 {
                    font-size: 16px;
                    }

                ```

            - Resultado: 

                - Aqui utilizamos o `font-size: 16px;` para definir que o tamanho da nossa font é 16px.

            

                



