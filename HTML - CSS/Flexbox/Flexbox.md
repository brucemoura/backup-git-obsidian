# Flex Container
> [!Summary] Sumário
> - Display
> - flex-direction
> - flex-wrap
> - flex-flow
> - justify-content
> - align-items
> - align-content

## Display
Define o elemento como um flex container, tornando seus FILHOS flex-itens.
![[HTML - CSS/Flexbox/imagens/img-01.png]]
```html
<body>
  <h1>Display: block;</h1>
  <section class="container">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
    <div class="item">4</div>
  </section>
  <h1>Display: flex;</h1>
  <section class="container flex">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
    <div class="item">4</div>
  </section>
  <h1>Display: flex;</h1>
  <section class="container flex">
    <div class="item">testeteste 1</div>
    <div class="item">testeteste 2</div>
    <div class="item">testeteste 3</div>
    <div class="item">testeteste 4</div>
    <div class="item">testeteste 1</div>
    <div class="item">testeteste 2</div>
    <div class="item">testeteste 3</div>
    <div class="item">testeteste 4</div>
  </section>
  <h1>Display: flex;</h1>
  <section class="container flex flex-wrap">
    <div class="item">testeteste 1</div>
    <div class="item">testeteste 2</div>
    <div class="item">testeteste 3</div>
    <div class="item">testeteste 4</div>
    <div class="item">testeteste 1</div>
    <div class="item">testeteste 2</div>
    <div class="item">testeteste 3</div>
    <div class="item">testeteste 4</div>
  </section>
  <h1>Display: flex; / flex-item-1</h1>
  <section class="container flex">
    <div class="item flex-item-1">1</div>
    <div class="item flex-item-1">2</div>
    <div class="item flex-item-1">3</div>
    <div class="item flex-item-1">4</div>
  </section>
</body>
```
```css
.container{
  max-width: 400px;
  margin: 0 auto;
  border: 1px solid black;
}

.item{
  background-color: rgb(53, 174, 255);
  color: black;
  text-align: center;
  margin: 3px;
}

h1{
  font-size: 18px;
  font-family: Arial, Helvetica, sans-serif;
  text-align: center;
}

/*****************************************/
/* flex */
.flex{
  display: flex;
  /*Torna o elemento um flex container automaticamente transformando todos os seus filhos diretos em flex itens.*/
}

.flex-wrap{
  flex-wrap: wrap;
}

.flex-item-1{
  flex: 1;
}
```
## Flex Direction
Define a direção dos flex itens. Por padrão ele é row(linha), por isso quando o `display:flex;` é adicionado, os elementos ficam em linha, um do lado do outro.
A mudança de row para column geralmente acontece quando estamos definindo os estilos em media queries para mobile.
Assim voce garante que o conteúdo seja apresentado em uma única coluna.
![[HTML - CSS/Flexbox/imagens/img-02.png]]
```html
<body>
  <h1>flex-direction: row;</h1>
  <section class="container row">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
    <div class="item">4</div>
  </section>
  <h1>flex-direction: row-reverse;</h1>
  <section class="container row-reverse">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
    <div class="item">4</div>
  </section>
  <h1>flex-direction: column;</h1>
  <section class="container column">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
    <div class="item">4</div>
  </section>
  <h1>flex-direction: column-reverse;</h1>
  <section class="container column-reverse">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
    <div class="item">4</div>
  </section>
</body>
```
```css
/* flex-direction */
  .row{
    flex-direction: row;
    /*Padrão os itens ficam em linha*/
  }
  .row-reverse{
    flex-direction: row-reverse;
    /*Os itens ficam em linha reversa*/
  }
  .column{
    flex-direction: column;
    /*Os itens ficam em coluna*/
  }
  .column-reverse{
    flex-direction: column-reverse;
    /*Os itens ficam em coluna reversa*/
  }
```
## Flex Wrap
Define se os itens devem quebrar ou não a linha. Por padrão eles não quebram, isso faz com que os itens sejam compactados além do limite, e dependendo do tamanho do conteúdo ele vai estourar a caixa.
Essa é geralmente uma propriedade que é quase sempre definida como `flex-wrap: wrap:` Pois assim quando um dos flex itens atinge o limite do conteúdo, o último passa para a coluna debaixo e assim por diante.
![[HTML - CSS/Flexbox/imagens/img-03.png]]
```html
<body>
  <h1>flex-wrap: nowrap;</h1>
  <section class="container nowrap">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
  <h1>flex-wrap: Wrap;</h1>
  <section class="container wrap">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
  <h1>flex-wrap: wrap-reverse;</h1>
  <section class="container wrap-reverse">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
</body>
```
```css
/* flex-wrap */
  .nowrap {
    flex-wrap: nowrap;
    /*Valor padrão, não permite a quebra de linha*/
  }

  .wrap {
    flex-wrap: wrap;
    /*Permite a quebra de linha assim que um dos itens não poder mais ser compactados*/
    
  }

  .wrap-reverse {
    flex-wrap: wrap-reverse;
    /*Permite a quebra de linha assim que um dos itens não poder mais ser compactados. A quebra de linha e na direção contratia, ou seja par a linha de cima*/	
  }
```
## Flex Flow
O `flex-flow` é um atalho para as propriedades flex-direction e flex-direction, não veremos muito seu uso porque quando mudamos o flex-direction para column, mantemos o padrão do flex-wrap que é nowrap. 
E Quando mudamos o flex-wrap para wrap, mantemos o padrão do flex-direction que é row.
![[HTML - CSS/Flexbox/imagens/img-04.png]]
``` html

  <h1>flex-flow: row-nowrap;</h1>
  <section class="container row-nowrap">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
  <h1>flex-flow: row-wrap;</h1>
  <section class="container row-wrap">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
  <h1>flex-flow: column-nowrap;</h1>
  <section class="container column-nowrap">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
```
```css
/* flex-flow */
  .row-nowrap {
    flex-flow: row nowrap;
    /* Coloca o conteúdo em linha e não permite a quebra de linha */
  }

  .row-wrap {
    flex-flow: row wrap;
    /* Coloca o conteúdo em linha e permite a quebra de linha */
  }

  .column-nowrap {
    flex-flow: column nowrap;
    /* Coloca o conteúdo em coluna e não permite a quebra de conteúdo */
  }
```
## Justify Content
Alinha os itens flex no container de acordo com a direção. A propriedade só funciona caso HAJA ESPAÇO LATERAL, isso significa que se os filhos de um item que tem a propriedade flex tiver a propriedade `flex:1;` (veremos sobre ela mais tarde) ela não vai funcionar.
Excelente propriedade para ser usada em caso que você deseja alinhar um item na ponta esquerda e outro na ponta direita, como um um simples header com marca e navegação.
![[HTML - CSS/Flexbox/imagens/img-05.png]]
```html

  <h1>justify-content: flex-start;</h1>
  <section class="container flex-start">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
  <h1>justify-content: flex-end;</h1>
  <section class="container flex-end">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
  <h1>justify-content: center;</h1>
  <section class="container center">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
  <h1>justify-content: space-between;</h1>
  <section class="container space-between">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
  <h1>justify-content: space-around;</h1>
  <section class="container space-around">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
  <h1>justify-content: space-evenly;</h1>
  <section class="container space-evenly">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
```
```css
/* justify-content */
  .flex-start {
    justify-content: flex-start;
    /* Alinha os itens ao início do container */
  }

  .flex-end {
    justify-content: flex-end;  
    /* Alinha os itens ao fim do container */
  }
  .center {
    justify-content: center;
    /* Alinha os itens ao centro do container */
  }

  .space-between {
    justify-content: space-between;
    /* Cria um espaçamento igual entre os elementos, mantendo o primeiro grudado ao início e o último grudado ao fim */
  }
  .space-around {
    justify-content: space-around;
    /* Cria um espaçamento igual entre os elementos. Os espaçamentos do meio são duas vezes maiores que o inicial e final */
  }

  .space-evenly {
    justify-content: space-evenly;  
    /* Cria um espaçamento igual entre os elementos. */
  }
```
## Aling Items
O `align-items` alinha os flex itens de acordo com o eixo do container. O alinhamento é diferente para quando os itens estão em colunas ou linhas.
Essa propriedade permite o tão sonhado alinhamento central no eixo vertical, algo que antes só era possível com diferentes hacks.
- em row
![[HTML - CSS/Flexbox/imagens/img-06.png]]
```html
  <h1>align-items: stretch;</h1>
  <section class="container stretch">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
  <h1>align-items: flex-start;</h1>
  <section class="container flex-start">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
  <h1>align-items: flex-end;</h1>
  <section class="container flex-end">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
  <h1>align-items: center;</h1>
  <section class="container center">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
  <h1>align-items: baseline;</h1>
  <section class="container baseline">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
```
```css
/* align-items */
  .stretch {
    align-items: stretch;
    /* Valor padrão, ele que faz com que os flex itens cresçam igualmente. */
  }

  .flex-start {
    align-items: flex-start;  
    /* Alinha os items ao início */
  }
  .flex-end {
    align-items: flex-end;
    /* Alinha os items ao final */
  }

  .center {
    align-items: center;
    /* Alinha os items ao centro*/
  }
  .baseline {
    align-items: baseline;
    /* Alinha os itens de acordo com a linha base da tipografia */
  }
```
- em column
![[HTML - CSS/Flexbox/imagens/img-07.png]]
```html
<h1>align-items: stretch; // column</h1>
  <section class="container stretch">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
  <h1>align-items: flex-start; // column</h1>
  <section class="container flex-start column">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
  <h1>align-items: flex-end; // column</h1>
  <section class="container flex-end column">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
  <h1>align-items: center; // column</h1>
  <section class="container center column">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
  <h1>align-items: baseline; // column</h1>
  <section class="container baseline column">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
```
```css
/* align-items */
  .stretch {
    align-items: stretch;
    flex-direction: column;
    /* Valor padrão, ele que faz com que os flex itens cresçam igualmente. */
  }

  .flex-start {
    align-items: flex-start;
    flex-direction: column;
    /* Alinha os items ao início */
  }

  .flex-end {
    align-items: flex-end;
    flex-direction: column;
    /* Alinha os items ao final */
  }

  .center {
    align-items: center;
    flex-direction: column;
    /* Alinha os items ao centro*/
  }

  .baseline {
    align-items: baseline;
    flex-direction: column;
    /* Alinha os itens de acordo com a linha base da tipografia */
  }
```
>[!note] column
>Para colocar os itens flex como coluna podemos fazer isso somente no pai do item.
- item alinhado ao centro do container
![[HTML - CSS/Flexbox/imagens/img-08.png]]
```html
<h1>justify-content:center; // align-items: center;</h1>
<section class="container centro">
	<div class="item">Este item está vertical e horizontalmente alinhado</div>
</section>
```
```css
  /* Alinhamento ao centro */
  .centro {
    justify-content: center;
    /* Alinha os itens ao centro do container horizontalmente*/
    align-items: center;
    /* Alinha os items ao centro verticalmente*/
  }
```
## Align Content
As linhas do container em relação ao eixo vertical. A propriedade só funciona se existir mais de uma linha flex-itens. Para isso o flex-wrap precisa ser wrap
Além disso o efeito dela apenas será visível caso o container seja maior que a soma das linhas dos itens, isso significa que se você não definir height para o container, a propriedade não influenciará no layout.
![[HTML - CSS/Flexbox/imagens/img-09.png]]
```html
<h1>align-content: stretch;</h1>
  <section class="container stretch">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
  <h1>align-content: flex-start;</h1>
  <section class="container flex-start">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
  <h1>align-content: flex-end;</h1>
  <section class="container flex-end">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
  <h1>align-content: center;</h1>
  <section class="container center">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
  <h1>align-content: space-between;</h1>
  <section class="container space-between">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
  <h1>align-content: space-around;</h1>
  <section class="container space-around">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
  <h1>align-content: space-evenly;</h1>
  <section class="container space-evenly">
    <div class="item">Testeeeedoditem1</div>
    <div class="item">Testeeeedoditem2</div>
    <div class="item">Testeeeedoditem3</div>
    <div class="item">Testeeeedoditem4</div>
    <div class="item">Testeeeedoditem4</div>
  </section>
```
```css
  /* align-content */
  .stretch {
    align-content: stretch;
    /* Valor padrão, ele que faz com que os flex itens cresçam igualmente. */
  }

  .flex-start {
    align-content: flex-start;
    /* Alinha os items ao início verticalmente*/
  }

  .flex-end {
    align-content: flex-end;
    /* Alinha os items ao final verticalmente*/
  }

  .center {
    align-content: center;
    /* Alinha os items ao centro verticalmente*/
  }

  .space-between {
    align-content: space-between;
    /* Cria um espaçamento igual entre os elementos, mantendo o primeiro grudado ao início e o último grudado ao fim */
  }

  .space-around {
    align-content: space-around;
    /* Cria um espaçamento igual entre os elementos. Os espaçamentos do meio são duas vezes maiores que o inicial e final */
  }

  .space-evenly {
    align-content: space-evenly;
    /* Cria um espaçamento igual entre os elementos. */
  }
```
# Flex Item
## Flex Grow
Define a habilidade de um flex-item crescer. Por padrão o valor é zero, assim os flex itens ocupam um tamanho máximo relacionado ao conteúdo interno deles ou ao width definido.
Ao definir 1 para todos os Flex itens, eles tentarão ter a mesma largura e vão ocupar 100% do container. Digo tentarão pois caso um elemento possua um conteúdo muito largo, ele irá respeitar o mesmo.
Se você tiver uma linha com 4 itens, onde três `flex-grow:1;` e um `flex-grow:2;` o `flex-grow: 2;` tentará ocupar 2 vezes mais espaço extra do que os outros elementos.
OBS: justify-content não funciona em items com flex-grow definido.
![[HTML - CSS/Flexbox/imagens/img-10.png]]
```html
  <h1>flex-grow: 0;</h1>
  <section class="container fg-0">
    <div class="item">Teste 1</div>
    <div class="item">Teste 2</div>
    <div class="item">Teste 3</div>
  </section>

  <h1>flex-grow: 1;</h1>
  <section class="container fg-1">
    <div class="item">Teste 1</div>
    <div class="item">Teste 2</div>
    <div class="item">Teste 3</div>
  </section>
  <h1>flex-grow: 2;</h1>
  <section class="container fg-2">
    <div class="item">Teste 1</div>
    <div class="item item-especial">Teste 2</div>
    <div class="item">Teste 3</div>
  </section>
```
```css
/*Flex grow*/
.fg-0 .item{
  flex-grow: 0;
}
.fg-1 .item, .fg-2 .item{
  flex-grow: 1;
}
.fg-2 .item-especial{
  flex-grow: 2;
}
```
>[!info] Lembrando que:  
>Quem será atacado será o item em que o pai dele e flex ou seja ele tem que ser um item flex.
## Flex Basis
indica o tamanho inicial do flex item antes da distribuição do espaço restante.
Quando definimos o `flex-grow: 1;` e possuímos o valor auto no basis, o valor restante para ocupar o container é distribuído ao redor do conteúdo do flex-item.
## Flex Shrink
Define a capacidade de redução de tamanho do item.
## Flex
Atalho para as propriedades: flex-grow, flex-shrink e flex-basis. Geralmente vemos a propriedade flex nos flex itens ao invés de cada valor separado.
Para melhor consistência entre os browsers, é recomendado utilizar a propriedade flex ao invés de cada unidade separada.
No exemplo é possível ver as mesmas configurações do exemplo do flex-basis porém agora utilizando apenas a propriedade flex.
![[HTML - CSS/Flexbox/imagens/img-11.png]]
```html
  <h1>flex: 1;</h1>
  <section class="container">
    <div class="item flex-1">1</div>
    <div class="item basis-auto">2</div>
    <div class="item basis-auto-grow-2">3</div>
    <div class="item ">4</div>
    <div class="item ">5</div>
  </section>
```
```css
/*Flex*/
.flex-1{
  flex: 1;
  /* Define flex-grow: 1; flex-shrink: 1; e flex-basis: 0; (em alguns browsers define como 0%, pois estes ignoram valores sem unidades, porém a função de 0 e 0% é a mesma)*/
}
.basis-auto{
  flex: 1 1 auto;
}
.basis-auto-grow-2{
  flex: 2 1 auto;
}
```
## order
Modifica a ordem dos flex-itens. Sempre do menor para o maior, assim order: 1; aparece na frente de order: 5;
![[HTML - CSS/Flexbox/imagens/img-12.png]]
```html
  <h1>order: 1;</h1>
  <section class="container">
    <div class="item order-1">1</div>
    <div class="item order-5">2</div>
    <div class="item order-2">3</div>
    <div class="item ">4</div>
    <div class="item ">5</div>
  </section>
  <h1>order: 1; // flex: 1;</h1>
  <section class="container">
    <div class="item flex-1 order-5">1</div>
    <div class="item flex-1 order-4">2</div>
    <div class="item flex-1 ">3</div>
    <div class="item flex-1 order-1">4</div>
    <div class="item flex-1 ">5</div>
  </section>
  <h1>order: 1; // column</h1>
  <section class="container column">
    <div class="item order-5">1</div>
    <div class="item order-3">2</div>
    <div class="item order-1">3</div>
    <div class="item order-2">4</div>
    <div class="item order-4">5</div>
  </section>
```
```css
/*Order*/
.order-1{
  order: 1;
}
.order-2{
  order: 2;
}
.order-3{
  order: 3;
}
.order-4{
  order: 4;
}
.order-5{
  order: 5;
}

.flex-1{
flex: 1;
}

.column{
  flex-direction: column;
}
```
## align-self
O align-self serve para definirmos o alinhamento especifico de um único flex item dentro do nosso container. Caso um valor seja atribuído, ele passará por cima do que for atribuído no align-items do container.
vale lembrar que o alinhamento acontece tanto em linha quanto em colunas, Por exemplo o flex-start quando os itens estão em linha, alinha o item ao topo de sua linha. Quando em colunas, alinha o item ao início(esquerda) da coluna.
![[HTML - CSS/Flexbox/imagens/img-13.png]]
```html
  <h1>align-self: multiplos:</h1>
  <section class="container">
    <div class="item flex-1 flex-center">1</div>
    <div class="item flex-1 flex-end">2 teste</div>
    <div class="item flex-1 ">3  amet consectetur adipisicing elit.</div>
    <div class="item flex-1 flex-baseline">teste 4</div>
  </section>
  <h1>align-self:stretch: // aling-items: flex-end;</h1>
  <section class="container aling-items-end">
    <div class="item flex-1 ">1</div>
    <div class="item flex-1 flex-stretch">2 teste</div>
    <div class="item flex-1 ">3  amet consectetur adipisicing elit.</div>
    <div class="item flex-1 ">teste 4</div>
  </section>
  <h1>align-self: multiplos: // column</h1>
  <section class="container column">
    <div class="item flex-1 flex-center">1</div>
    <div class="item flex-1 flex-end">2 teste</div>
    <div class="item flex-1 ">3  amet consectetur adipisicing elit.</div>
    <div class="item flex-1 flex-baseline">teste 4</div>
  </section>
  <h1>align-self: multiplos: // column</h1>
  <section class="container column">
    <div class="item flex-1 flex-start">1</div>
    <div class="item flex-1 flex-end">2 teste</div>
    <div class="item flex-1 ">3  amet consectetur adipisicing elit.</div>
    <div class="item flex-1 flex-baseline">teste 4</div>
  </section>
  <h1>align-self:stretch: // aling-items: flex-end;</h1>
  <section class="container column aling-items-end">
    <div class="item flex-1 ">1</div>
    <div class="item flex-1 flex-stretch">2 teste</div>
    <div class="item flex-1 ">3  amet consectetur adipisicing elit.</div>
    <div class="item flex-1 ">teste 4</div>
  </section>
```
```css
/*Align Self*/
.column{
  flex-direction: column;
}
.flex-1{
  flex: 1;
}
.flex-start{
  align-self: flex-start;
}
.flex-end{
  align-self: flex-end;
}
.flex-center{
  align-self: center;
}
.flex-baseline{
  align-self: baseline;
}
.flex-stretch{
  align-self: stretch;
}

.aling-items-end{
  align-items: flex-end;
}
.aling-items-start{
  align-items: flex-start;
}
```





















