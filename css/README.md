# Documentação sobre CSS3

## índices

00. [O que é o CSS3 e como usá-lo](#documentação-sobre-css3)
01. [Cores e estilos básicos](#corres-e-estilos-básicos)
02. [DevTools](#devtools)
03. [Cores](#cores)
04. [Background e Border](#background-e-border)
05. [Unidade de medida]()
06. [Especificidade]()


## O que é o HTML e como usá-lo

#### O que é CSS?

- A sigla `css` significa `Cascading Styles Sheets` ou folhas de estilo em cascata.

- A linaguagem é usada para definir os estilos em um documento `html

- Pode ser incluido no documento de 3 modos:

    - Utilizando o atríbuto style, por exemplo:

        ```css

            <h1 style="color: red;">Título Vermelho</h1>
        
        ```

        - Aqui utilizamos a tag `h1` com a junção do atríbuto de `style="color"` para definição de uma cor ao nosso título.

    - Com a tag `style`, por exemplo:

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

        - Com a tag `style`, podemos aplicar regras de `css` diretamente dentro do documento `html`, sem precisar de um arquivo externo. Ela deve ser colocada dentro da tag `head`, que é responsável por conter as informações de configuração e estilo da página.

    - Utilizando a tag link apontando para um arquivo `css` que é o mais comum, por exemplo:

        ```css

            <link rel="stylesheet" href="style.css">

        ```

        - Adicionamos a tag `link` para linkar ao nosso `html` e apontamos para o nosso arquivo css com o atríbuto `href=""`, e o atríbuto `rel=stylesheet` informa ao navegador que é uma folha de estilo `css`.

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

    - 1 Utilizando via a tag `link`
    - 2 Utilizando via atríbuto `style`

- A forma mais comum é criando um arquivo serpado para utiização do código `css` atráves da tag `link` apontando para o mesmo.

    - Exemplo:

        ```css

            <link rel="stylesheet" href="../001_comeco.css"> <!-- Linkando o ccs por link no arquivo-->
        
        ```
    
    - Utilizando o atríbuto `href=""` para apontar ao destino do arquivo `css` de forma absoluta.

### Cores diretamente no arquivo `css`

- Vale ressaltar que o `css` é em castaca, então a última propriedade definida para determinada tag vai ser a alterada.

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

- Posso altera isso de forma temporária, basta selecionar a tag desejada no `Elements` e alterar o estilo dela no `Styles`, para alterar o `html` é no `Elements` e no `css` no `Estyles`.

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

        - Observa-se que selecionamos novamente a tag `p` e ali temos todas as suas propriedades e seu tamanho.

        - margin, border, padding

            ![marginbordepadding](../css/assets/imagens/MarginBorderPadding.png)

        - margin:

            - Todas as tags possuem `margin`, que nada mais é que o espaçamento entre as laterais, superior e inferior ao elemento.

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

        - Sabemos que o `color` muda a cor dos nomes, enquanto o `background` muda o background de fundo de uma tag definida. Vale resltar que o `backgroud` funciona tanto com tags `html` quando com atríbutos, só que com atríbutos só irá funciona caso seja definido um `id` para o atríbuto desejado.

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

    - A propriedade `border` é utilizada para definir a borda de um elemento(tag ou atríbutos com `id`) no `html`, geralmente utilizada para aplicar no elemento para ter as suas características alteradas como o seu tamanho, a sua cor ou seu estilo.

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





