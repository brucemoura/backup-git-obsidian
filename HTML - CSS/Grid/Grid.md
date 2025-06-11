# Flex Container
> [!Summary] Sumário
> - display
> - Grid Container
> - Grid Item
# display
Define o elemento como um grid container.
```css
.grid{
  display: grid; /* Torna o elemento um grid container */
}
```
![[HTML - CSS/Grid/imagens/img-01.png]]
```html
  <div class="margin">
    <h1>display: grid; </h1>
    <div class="grid container">
      <div class="item">1</div>
      <div class="item">2</div>
      <div class="item">3</div>
      <div class="item">4</div>
    </div>
  </div>

  <div class="margin">
    <h1>display: grid; // grid-template-columns: 200px 200px;</h1>
    <div class="grid container grid-template-columns">
      <div class="item">1</div>
      <div class="item">2</div>
      <div class="item">3</div>
      <div class="item">4</div>
    </div>
  </div>

  <div class="margin">
    <h1>display: grid; // grid-template-columns: 25% 50% 25%;</h1>
    <div class="grid container grid-template-columns-porcentagem">
      <div class="item">1</div>
      <div class="item">2</div>
      <div class="item">3</div>
    </div>
  </div>
  
  <div class="margin">
    <h1>display: grid; // grid-template-columns: 1fr;</h1>
    <div class="grid container grid-template-columns-fr11">
      <div class="item">1</div>
      <div class="item">2</div>
      <div class="item">3</div>
      <div class="item">4</div>
      <div class="item">5</div>
      <div class="item">6</div>
    </div>
  </div>

  <div class="margin">
    <h1>display: grid; // grid-template-columns: 1fr 2fr 1fr;</h1>
    <div class="grid container grid-template-columns-fr121">
      <div class="item">1</div>
      <div class="item">2</div>
      <div class="item">3</div>
      <div class="item">4</div>
      <div class="item">5</div>
      <div class="item">6</div>
    </div>
  </div>
  
  <div class="margin">
    <h1>display: grid; // grid-template-columns: 1fr 2fr 1fr; + subgrid </h1>
    <div class="grid container grid-template-columns-fr121">
      <div class="item">1</div>
      <div class="item">2</div>
      <div class="item">3</div>
      <div class="item">4</div>
      <div class="color2 grid grid-template-columns-fr121">
        <div class="item">5.1</div>
        <div class="item">5.2</div>
        <div class="item">5.3</div>
      </div>
      <div class="item">6</div>
    </div>
  </div>
```
```css
* {
  font-family: monospace;
  margin: 0;
  padding: 0;
}

body {
  padding: 30px;
}

.margin {
  margin: 30px 0;
}

h1 {
  text-align: center;
  font-size: 1.6rem;
  font-weight: 100;
}

.container {
  display: block; /* Torna o elemento um grid container */
  border: 1px solid black;
  max-width: 500px;
  margin: 0 auto;
}

.container > div {
  text-align: center;
  margin: 5px;
  background-color: rgb(53, 174, 255);
  padding: 5px;
  font-size: 1.4rem;
}

/* **************************************** */
.grid {
  display: grid;
}

.grid-template-columns {
  grid-template-columns: 200px 200px;
}

.grid-template-columns-porcentagem {
  grid-template-columns: 25% 50% 25%;
}

.grid-template-columns-fr11 {
  grid-template-columns: 1fr 1fr;
}
.grid-template-columns-fr121 {
  grid-template-columns: 1fr 2fr 1fr;
}

.color2 {
  gap: 5px;
}

.color2 > div {
  background-color: aqua;
}

```

# Grid Container
O Grid Container é a tag que envolve os itens do grid, ao indicar `display: grid;` essa tag passa a ser um Grid Container. 
## Grid Template Columns
Define o número total de colunas que serão criadas no grid.
![[HTML - CSS/Grid/imagens/img-02.png]]
```html
<div class="margin">
	<h1>display: grid; // grid-template-columns: 200px 200px;</h1>
    <div class="grid container grid-template-columns">
      <div class="item">1</div>
      <div class="item">2</div>
      <div class="item">3</div>
      <div class="item">4</div>
    </div>
</div>

  <div class="margin">
    <h1>display: grid; // grid-template-columns: 25% 50% 25%;</h1>
    <div class="grid container grid-template-columns-porcentagem">
      <div class="item">1</div>
      <div class="item">2</div>
      <div class="item">3</div>
    </div>
  </div>
  
  <div class="margin">
    <h1>display: grid; // grid-template-columns: 1fr 1fr;</h1>
    <div class="grid container grid-template-columns-fr11">
      <div class="item">1</div>
      <div class="item">2</div>
      <div class="item">3</div>
      <div class="item">4</div>
      <div class="item">5</div>
      <div class="item">6</div>
    </div>
  </div>

  <div class="margin">
    <h1>display: grid; // grid-template-columns: 1fr 2fr 1fr;</h1>
    <div class="grid container grid-template-columns-fr121">
      <div class="item">1</div>
      <div class="item">2</div>
      <div class="item">3</div>
      <div class="item">4</div>
      <div class="item">5</div>
      <div class="item">6</div>
    </div>
  </div>
  
  <div class="margin">
    <h1>display: grid; // grid-template-columns: 1fr 2fr 1fr; + grid </h1>
    <div class="grid container grid-template-columns-fr121">
      <div class="item">1</div>
      <div class="item">2</div>
      <div class="item">3</div>
      <div class="item">4</div>
      <div class="color2 grid grid-template-columns-fr121">
        <div class="item">5.1</div>
        <div class="item">5.2</div>
        <div class="item">5.3</div>
      </div>
      <div class="item">6</div>
    </div>
  </div>

  <div class="margin">
    <h1>display: grid; // grid-template-columns:minmax(200px, 1fr) 3fr 2fr; </h1>
    <div class="grid container gtc-minmax">
      <div class="item">1</div>
      <div class="item">2</div>
      <div class="item">3</div>
      <div class="item">4</div>
      <div class="item">5</div>
      <div class="item">6</div>
    </div>
  </div>
  
  <div class="margin">
    <h1>display: grid; // grid-template-columns:repeat(3, 1fr); </h1>
    <div class="grid container gtc-repeat">
      <div class="item">1</div>
      <div class="item">2</div>
      <div class="item">3</div>
      <div class="item">4</div>
      <div class="item">5</div>
      <div class="item">6</div>
    </div>
  </div>

  <div class="margin">
    <h1>display: grid; // grid-template-columns:repeat(auto-fit, minmax(100px, auto)); </h1>
    <div class="grid container gtc-auto">
      <div class="item">1</div>
      <div class="item">2</div>
      <div class="item">3</div>
      <div class="item">4</div>
      <div class="item">5</div>
      <div class="item">6</div>
    </div>
  </div>
```
```css
  /* display: grid; */

  .grid-template-columns {
    grid-template-columns: 200px 200px;
    /* 2 colunas de 200px  são criadas*/
  }

  .grid-template-columns-porcentagem {
    grid-template-columns: 25% 50% 25%;
    /* 2 Colunas com cada uma com 25% 50% e 25% são criadas*/
  }

  .grid-template-columns-fr11{
    grid-template-columns: 1fr 1fr;
    /* 2 colunas são criadas, cada uma com metade (fr = é uma unidade fracional ou seja se tivermos 2fr 2fr será o mesmo tamanho (50%), mas se for 1fr 2fr sera (33% e 66%), então se o n° de fr for o mesmo a porcentage também será mas se for diferente a porcentagem será diferente.) */
  }
  .grid-template-columns-fr121{
    grid-template-columns: 1fr 2fr 1fr;
    /* 3 colunas são criadas, uma com 1fr outra com 2fr e a última com 1fr, funciona do mesmo jeito que foi explicado acima.*/
  }
  .gtc-minmax{
    grid-template-columns: minmax(200px, 1fr) 3fr 2fr;
    /* 3 colunas são criadas, a primeira terá no mínimo 200px e no maxímo 1fr(isso significa que após 200px ela se expande da mesma forma que as outras colunas). As outras duas colunas vão ter 1fr */
  }
  .gtc-repeat{
    grid-template-columns: repeat(3, 1fr);
    /* 3 colunas são criadas com 1fr de tamanho. O repeat seria a mesma coisa que 1fr 1fr 1fr.*/
  }
  .gtc-auto{
    grid-template-columns: repeat(auto-fit, minmax(100px, auto));
    /* Cria automaticamente um total de colunas que acomode itens com no mínimo 100px de largura.
     */
  }
```
## Grid Template Rows
Define a quantidade de linhas no grid.
![[HTML - CSS/Grid/imagens/img-03.png]]
```html
  <div class="margin">
    <h1>display: grid; // grid-template-rows: 200px 200px;</h1>
    <div class="grid container grid-template-rows">
      <div class="item">1</div>
      <div class="item">2</div>
      <div class="item">3</div>
      <div class="item">4</div>
      <div class="item">5</div>
      <div class="item">6</div>
    </div>
  </div>

  <div class="margin">
    <h1>display: grid; // grid-template-rows: 1fr 2fr 1fr;</h1>
    <div class="grid container grid-template-rows-porcentagem">
      <div class="item">1</div>
      <div class="item">2</div>
      <div class="item">3</div>
    </div>
  </div>
  
  <div class="margin">
    <h1>display: grid; // grid-t-rows e grid-t-columns</h1>
    <div class="grid container grid-template-rows-column">
      <div class="item">1</div>
      <div class="item">2</div>
      <div class="item">3</div>
      <div class="item">4</div>
      <div class="item">5</div>
      <div class="item">6</div>
      <div class="item">7</div>
      <div class="item">8</div>
      <div class="item">9</div>
    </div>
  </div>
```
```css
/* grid Rows */
  .grid-template-rows {
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 60px 100px;
    /* 2 Linhas de 60px e 100px são criadas, caso o grid necessite de mais linhas elas serão criadas de acordo com o conteúdo.*/
  }

  .grid-template-rows-porcentagem {
    grid-template-rows: 1fr 2fr 1fr;
    /* 3 Linhas sendo a 2 linha com duas vezes o tamanho da primeira e da última*/
  }

  .grid-template-rows-column {
    grid-template-columns: 100px auto 50px;
    grid-template-rows: 50px 200px 50px;
  }
```
## Grid Template Areas
Define áreas específicas no grid. O ponto(.) pode ser utilizado para criar áreas vazias.
![[HTML - CSS/Grid/imagens/img-04.png]]
```html
<div class="margin">
  <h1>display: grid; // grid-template-areas</h1>
  <div class="grid container grid-template-areas">
    <div class="item logo">logo</div>
    <div class="item nav">nav</div>
    <div class="item sidnav">sidnav</div>
    <div class="item content">content</div>
    <div class="item advert">advert</div>
    <div class="item footer">footer</div>
  </div>
</div>
```
```css
  /* grid areas */
  .grid-template-areas {
    grid-template-areas:
      "logo nav nav"
      "sidnav content advert"
      "sidnav footer footer";
      /* cria 3 colunas e 3 linhas:
      [logo ocupa a 1° linha e a 1° coluna],
      [nav ocupa a 1° coluna a 2° e 3° linha], 
      [sidnav ocupa a 2° e 3° coluna e 1° linha], 
      [content ocupa a 2° coluna e 2° linha], 
      [advert ocupa a 3° coluna e 2° linha], 
      [footer ocupa a 3° coluna e 2° e 3° linha]. */
  }
  .logo{
    grid-area: logo;
  }
  
  .nav{
    grid-area: nav;
  }
  
  .sidnav{
    grid-area: sidnav;
  }
  
  .content{
    grid-area: content;
  }
  
  .advert{
    grid-area: advert;
  }
  
  .footer{
    grid-area: footer;
  }
```
## Grid template
Atalho para definir o grid template columns, grows e areas.
![[HTML - CSS/Grid/imagens/img-05.png]]
```html
<div class="margin">
  <h1>display: grid; // grid-template-areas</h1>
  <div class="grid container grid-template-areas2">
    <div class="item logo2">logo</div>
    <div class="item nav2">nav</div>
    <div class="item sidnav2">sidnav</div>
    <div class="item content2">content</div>
    <div class="item advert2">advert</div>
    <div class="item footer2">footer</div>
  </div>
</div>
```
```css
  .grid-template-areas2{
    grid-template:
      "logo nav nav" 50px
      "sidnav content advert" 150px
      "sidnav footer footer" 100px
      / 100px 1fr 50px;
      /* 
        A 1° linha com 50px, a 2° linha com 150px e a 3° linha com 100px 
        / a 1° coluna com 100px, a 2° coluna com 1fr e a 3° coluna com 50px
      */
      /* A barra"/" separa o que e linha de coluna. */
  }
  .logo2{
    grid-area: logo;
  }
  
  .nav2{
    grid-area: nav;
  }
  
  .sidnav2{
    grid-area: sidnav;
  }
  
  .content2{
    grid-area: content;
  }
  
  .advert2{
    grid-area: advert;
  }
  
  .footer2{
    grid-area: footer;
  }
  
```
## Gap
Define o gap(gutter/espaçamento) entre os elementos do grid(e também funciona no flex).
![[HTML - CSS/Grid/imagens/img-06.png]]
```html
<div class="margin">
  <h1>display: grid; // gap: 10px;</h1>
  <div class="grid container grid-template-areas">
    <div class="item logo">logo</div>
    <div class="item nav">nav</div>
    <div class="item sidnav">sidnav</div>
    <div class="item content">content</div>
    <div class="item advert">advert</div>
    <div class="item footer">footer</div>
  </div>
</div>


<div class="margin">
  <h1>display: grid; // grid-template-areas</h1>
  <div class="grid container grid-template-areas2">
    <div class="item logo2">logo</div>
    <div class="item nav2">nav</div>
    <div class="item sidnav2">sidnav</div>
    <div class="item content2">content</div>
    <div class="item advert2">advert</div>
    <div class="item footer2">footer</div>
  </div>
</div>
```
```css
  /* grid areas */
  .grid-template-areas {
    grid-template-areas:
      "logo nav nav"
      "sidnav content advert"
      "sidnav footer footer";
	gap: 10px;
	column-gap: 40px;
	/*Define 40px de distância entre as colunas*/
    row-gap: 60px;
	/*Define 60px de distância entre as linhas*/
      
  }
  

  .container.grid-template-areas2{
    grid-template:
      "logo nav nav" 50px
      "sidnav content advert" 150px
      "sidnav footer footer" 100px
      / 100px 1fr 50px;
      gap: 30px;
  }
```
## Grid Auto Columns
Define o tamanho dos colunas do grid implícito(gerado automaticamente, quando algum elemento é posicionado em uma coluna que não foi definida).
![[HTML - CSS/Grid/imagens/img-07.png]]
```html
  <div class="margin">
    <h1>display: grid; // grid-auto-columns: 100px;</h1>
    <div class="grid container grid-auto-clumns-1">
      <div class="item ">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
      <div class="item ">4</div>
      <div class="item ">5</div>
      <div class="item grid-clumn-6">6</div>
    </div>
  </div>

  <div class="margin">
    <h1>display: grid; // grid-auto-columns: 50px 100px;</h1>
    <div class="grid container grid-auto-clumns-2">
      <div class="item ">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
      <div class="item ">4</div>
      <div class="item ">5</div>
      <div class="item grid-clumn-6">6</div>
    </div>
  </div>
  
  <div class="margin">
    <h1>display: grid; // grid-auto-columns não definido</h1>
    <div class="grid container grid-auto-clumns-3">
      <div class="item ">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
      <div class="item ">4</div>
      <div class="item ">5</div>
      <div class="item grid-clumn-6">6</div>
    </div>
  </div>
```
```css
 .grid-auto-clumns-1 {
    grid-template-columns: 1fr 1fr;
    grid-auto-columns: 100px;
    /* As duas primeiras colunas ocupam 1fr, e todas as colunas posteriores que forem sendo criadas ocuparão 100px */
  }

  .grid-auto-clumns-2 {
    grid-template-columns: 1fr 1fr;
    grid-auto-columns: 50px 100px;
    /* As duas primeiras colunas ocupam 1fr, e todas as colunas posteriores que forem sendo criadas ocuparão 50px e 100px alternando entre si */
  }

  .grid-auto-clumns-3 {
    grid-template-columns: 1fr 1fr;
    /* Não definido */
  }

  .grid-clumn-6 {
    grid-column: 6;
  }
```
## Grid Auto Rows
Define o tamanho das linhas do grid implícito (gerado automaticamente, quando algum elemento é posicionado em uma coluna que não foi definida).
![[HTML - CSS/Grid/imagens/img-08.png]]
```html
  <div class="margin">
    <h1>display: grid; // grid-auto-rows: 35px;</h1>
    <div class="grid container grid-auto-rows-1">
      <div class="item ">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
      <div class="item ">4</div>
      <div class="item ">5</div>
    </div>
  </div>

  <div class="margin">
    <h1>display: grid; // grid-auto-rows: 40px 70px;</h1>
    <div class="grid container grid-auto-rows-2">
      <div class="item ">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
      <div class="item ">4</div>
      <div class="item ">5</div>
    </div>
  </div>

  <div class="margin">
    <h1>display: grid; // grid-auto-rows não definido</h1>
    <div class="grid container grid-auto-rows-3">
      <div class="item ">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
      <div class="item ">4</div>
      <div class="item ">5</div>
    </div>
  </div>
```
```css
  .grid-auto-rows-1 {
    grid-template-rows: 1fr 1fr;
    grid-auto-rows: 35px;
    /* As duas primeiras colunas ocupam 1fr, e todas as colunas posteriores que forem sendo criadas ocuparão 100px */
  }

  .grid-auto-rows-2 {
    grid-template-rows: 1fr 1fr;
    grid-auto-rows: 40px 70px;
    /* As duas primeiras colunas ocupam 1fr, e todas as colunas posteriores que forem sendo criadas ocuparão 50px e 100px alternando entre si */
  }

  .grid-auto-rows-3 {
    /* Não definido */
  }
```
## Grid Auto Flow
Define o fluxo dos itens no grid. Se eles vão automaticamente gerar novas linhas ou colunas.
![[HTML - CSS/Grid/imagens/img-09.png]]
``` html
  <div class="margin">
    <h1>display: grid; // grid-auto-flow: column;</h1>
    <div class="grid container grid-auto-flow-1">
      <div class="item ">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
      <div class="item ">4</div>
      <div class="item ">5</div>
    </div>
  </div>

  <div class="margin">
    <h1>display: grid; // grid-auto-flow: row;</h1>
    <div class="grid container grid-auto-flow-2">
      <div class="item ">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
      <div class="item ">4</div>
      <div class="item ">5</div>
    </div>
  </div>

  <div class="margin">
    <h1>display: grid; // grid-auto-flow: dense;</h1>
    <div class="grid container grid-auto-flow-3">
      <div class="item ">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
      <div class="item ">4</div>
      <div class="item ">5</div>
    </div>
  </div>
```
```css
.grid-auto-flow-1{
  grid-auto-flow: column;
  /* Automaticamente gera novas colunas */
}

.grid-auto-flow-2{
  grid-auto-flow: row;
  /* Automaticamente gera novas linhas */
}

.grid-auto-flow-3{
  grid-auto-flow: dense;
  /* Tenta posicionar o mácimo dos elementos que existirem nas primeiras partes do grid (pode desorganizar o conteúdo). */
```
## Grid
Atalho geral para grid-template-rows, grid-template-columns, grid-template-areas, grid-auto-rows, grid-auto-columns e grid-auto-flow
![[HTML - CSS/Grid/imagens/img-10.png]]
```html
  <div class="margin">
    <h1>display: grid; // grid-auto-flow: column;</h1>
    <div class="grid container grid-auto-flow-1">
      <div class="item ">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
      <div class="item ">4</div>
      <div class="item ">5</div>
    </div>
  </div>

  <div class="margin">
    <h1>display: grid; // grid-auto-flow: row;</h1>
    <div class="grid container grid-auto-flow-2">
      <div class="item ">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
      <div class="item ">4</div>
      <div class="item ">5</div>
    </div>
  </div>

  <div class="margin">
    <h1>display: grid; // grid-auto-flow: dense;</h1>
    <div class="grid container grid-auto-flow-3">
      <div class="item ">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
      <div class="item ">4</div>
      <div class="item ">5</div>
    </div>
  </div>
```
```css
.grid-auto-flow-1{
  grid-auto-flow: column;
  /* Automaticamente gera novas colunas */
}

.grid-auto-flow-2{
  grid-auto-flow: row;
  /* Automaticamente gera novas linhas */
}

.grid-auto-flow-3{
  grid-auto-flow: dense;
  /* Tenta posicionar o mácimo dos elementos que existirem nas primeiras partes do grid (pode desorganizar o conteúdo). */
}
```
## Justify Content
Justifica os itens do grid em relação ao eixo X (horizontal). Lembrando que esses itens só poderão ser posicionados quando eles tiverem espaço, ou seja se nossos itens forem 1fr, auto ou qualquer outro valor que faça ele ocupar 100% do espaço.
![[HTML - CSS/Grid/imagens/img-11.png]]
```html
  <div class="margin">
    <h1>display: grid; // flex-start;</h1>
    <div class="grid container flex-start">
      <div class="item ">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
    </div>
  </div>

  <div class="margin">
    <h1>display: grid; // flex-end;</h1>
    <div class="grid container flex-end">
      <div class="item ">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
    </div>
  </div>

<div class="margin">
    <h1>display: grid; // stretch;</h1>
    <div class="grid container stretch">
      <div class="item ">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
    </div>
  </div>

  <div class="margin">
    <h1>display: grid; // center;</h1>
    <div class="grid container center">
      <div class="item ">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
    </div>
  </div>
  

  <div class="margin">
    <h1>display: grid; // space-between;</h1>
    <div class="grid container space-between">
      <div class="item ">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
    </div>
  </div>

  <div class="margin">
    <h1>display: grid; // space-evenly;</h1>
    <div class="grid container space-evenly">
      <div class="item ">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
    </div>
  </div>
  <div class="margin">
    <h1>display: grid; // space-around;</h1>
    <div class="grid container space-around">
      <div class="item ">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
    </div>
  </div>
```
```css
    /* justify-content */
  .flex-start {
    justify-content: flex-start;
    /* Alinha os itens ao início do container horizontalmente*/
  }

  .flex-end {
    justify-content: flex-end;  
    /* Alinha os itens ao fim do container horizontalmente*/
  }

  .streach {
    justify-content: stretch;
    /* Estica os itens.*/
  }

  .center {
    justify-content: center;
    /* Alinha os itens ao centro do container horizontalmente*/
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
## Aling Content
A mesma coisa que o justify content mas no eixo y (vertical)
![[HTML - CSS/Grid/imagens/img-12.png]]
```css
  .flex-start {
    align-content: flex-start;
    /* Alinha os itens ao início do container horizontalmente*/
  }

  .flex-end {
    align-content: flex-end;  
    /* Alinha os itens ao fim do container horizontalmente*/
  }

  .streach {
    align-content: stretch;
    /* Estica os itens.*/
  }

  .center {
    align-content: center;
    /* Alinha os itens ao centro do container horizontalmente*/
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
## Justify Items
Justifica o conteúdo dos itens do grid em relação ao eixo x (horizontal). Justifica em relação a célula.
![[HTML - CSS/Grid/imagens/img-13.png]]
```css
  .container{
    grid-auto-flow: column;
  }

    /* justify-items */
  .flex-start {
    justify-items: start;
    /* Alinha os itens ao início do container horizontalmente*/
  }

  .flex-end {
    justify-items: end;  
    /* Alinha os itens ao fim do container horizontalmente*/
  }

  .streach {
    justify-items: stretch;
    /* Estica os itens.*/
  }

  .center {
    justify-items: center;
    /* Alinha os itens ao centro do container horizontalmente*/
  }
```
## Align Items
Mesma coisa do Justify Items mas no eixo y (vertical)
![[HTML - CSS/Grid/imagens/img-14.png]]
```css
  .container{
    height: 200px;
    grid-auto-flow: row;
  }

    /* align-items */
  .flex-start {
    align-items: start;
    /* Alinha os itens ao início do container horizontalmente*/
  }

  .flex-end {
    align-items: end;  
    /* Alinha os itens ao fim do container horizontalmente*/
  }

  .streach {
    align-items: stretch;
    /* Estica os itens.*/
  }

  .center {
    align-items: center;
    /* Alinha os itens ao centro do container horizontalmente*/
  }

```
# Gird Item
Os Grid Itens são filhos diretos do Grid Container. Um grid item pode ser explicito ou implícito, Explicito e quando definimos ele no container e implícito e quando ele é criado automaticamente para preencher o conteúdo no grid.
## Grid Column
Define quais colunas serão ocupadas pelo grid item. É possível definir uma linha de início e final, assim o item ocupara múltiplas colunas.
![[HTML - CSS/Grid/imagens/img-15.png]]
```html
<div class="margin">
    <h1>display: grid; // grid-column: 1;</h1>
    <div class="grid container">
      <div class="item grid-column-1">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
    </div>
  </div>

  <div class="margin">
    <h1>display: grid; // grid-column: 1 / 3;</h1>
    <div class="grid container ">
      <div class="item grid-column-1-3">1</div>
      <div class="item">2</div>
      <div class="item">3</div>
    </div>
  </div>

<div class="margin">
    <h1>display: grid; // grid-column: 1 / -1;</h1>
    <div class="grid container ">
      <div class="item grid-column-1-1">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
    </div>
  </div>

  <div class="margin">
    <h1>display: grid; // grid-column-start: 2;</h1>
    <div class="grid container ">
      <div class="item grid-column-start">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
    </div>
  </div>
  
  <div class="margin">
    <h1>display: grid; // grid-column-end: 4;</h1>
    <div class="grid container ">
      <div class="item grid-column-end">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
    </div>
  </div>
  
  <div class="margin">
    <h1>display: grid; // grid-column: span 3;</h1>
    <div class="grid container ">
      <div class="item grid-column-span">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
    </div>
  </div>
```
```css
  .grid-column-1{
    grid-column: 1;
    /* O item ocupará a coluna 1*/
  }
  .grid-column-1-3{
    grid-column: 1 / 3;
    /* O item ocupará a coluna 1*/
  }
  .grid-column-1-1{
    grid-column: 1/-1;
    /* O item ocupará a coluna 1*/
  }
  .grid-column-start{
    grid-column-start: 2;
  }
  .grid-column-end{
    grid-column-end: 4;
  }
  .grid-column-span{
    grid-column: span 3;
  }
```
## Grid row
Define quais linhas serão ocupadas pelo grid item.
Atenção aqui, pois essa linha é referente a row. Porém as chamadas grid lines que por tradução também possui sempre 2 grid lines (linhas de grid), uma no início dela e outro no fim.
![[HTML - CSS/Grid/imagens/img-16.png]]
```html
  <div class="margin">
    <h1>display: grid; // grid-row: 1;</h1>
    <div class="grid container">
      <div class="item grid-row-1">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
    </div>
  </div>

  <div class="margin">
    <h1>display: grid; // grid-row: 1 / 3;</h1>
    <div class="grid container ">
      <div class="item grid-row-1-3">1</div>
      <div class="item">2</div>
      <div class="item">3</div>
    </div>
  </div>

<div class="margin">
    <h1>display: grid; // grid-row: 1 / -1;</h1>
    <div class="grid container">
      <div class="item grid-row-1-1">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
    </div>
  </div>

  <div class="margin">
    <h1>display: grid; // grid-row-start: 2;</h1>
    <div class="grid container ">
      <div class="item grid-row-start">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
    </div>
  </div>
  
  <div class="margin">
    <h1>display: grid; // grid-row-end: 4;</h1>
    <div class="grid container ">
      <div class="item grid-row-end">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
    </div>
  </div>
  
  <div class="margin">
    <h1>display: grid; // grid-row: span 3;</h1>
    <div class="grid container ">
      <div class="item grid-row-span">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
    </div>
  </div>
```
```css
  .grid-row-1{
    grid-row: 1;
    /* O item ocupará a coluna 1*/
  }
  .grid-row-1-3{
    grid-row: 1 / 3;
    /* O item ocupará a coluna 1*/
  }
  .grid-row-1-1{
    grid-row: 1/-1;
    /* O item ocupará a coluna 1*/
  }
  .grid-row-start{
    grid-row-start: 2;
  }
  .grid-row-end{
    grid-row-end: 4;
  }
  .grid-row-span{
    grid-row: span 3;
  }
```
## Grid Area
Define uma área do item do grid. É um atalho para grid-row-start, grid-column-start, grid-row-end e grid-column-end.
O z-index pode ser utilizado para manipular a posição no eixo Z do item, Ou seja se um item for posicionado em cima de outro, o z-index controla qual vêm na frente.
## Justify Self
Justifica o item do grid em relação ao eixo X (horizontal). Justifica em relação a célula
![[HTML - CSS/Grid/imagens/img-17.png]]
```html
  <div class="margin">
    <h1>display: grid; // justify-self: flex-start;</h1>
    <div class="grid container stretch">
      <div class="item justify-self-start">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
    </div>
  </div>
  <div class="margin">
    <h1>display: grid; // justify-self: flex-end;</h1>
    <div class="grid container stretch">
      <div class="item justify-self-end">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
    </div>
  </div>
  <div class="margin">
    <h1>display: grid; // justify-self: flex-center;</h1>
    <div class="grid container stretch">
      <div class="item justify-self-center">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
    </div>
  </div>
  <div class="margin">
    <h1>display: grid; // justify-self: flex-stretch;</h1>
    <div class="grid container stretch">
      <div class="item justify-self-stretch">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
    </div>
  </div>
```
```css
  .streach {
    justify-items: stretch;
    /* Estica os itens.*/
  }

  .justify-self-start {
    justify-self: start;
  }
  .justify-self-end {
    justify-self: end;
  }
  .justify-self-center {
    justify-self: center;
  }
  .justify-self-stretch {
    justify-self: stretch;
  }
```
## Align Self
mesma coisa do justify self mas em relação ao eixo Y (vertical)
![[HTML - CSS/Grid/imagens/img-18.png]]
```html
  <div class="margin">
    <h1>display: grid; // align-self: flex-start;</h1>
    <div class="grid container stretch">
      <div class="item align-self-start">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
    </div>
  </div>
  <div class="margin">
    <h1>display: grid; // align-self: flex-end;</h1>
    <div class="grid container stretch">
      <div class="item align-self-end">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
    </div>
  </div>
  <div class="margin">
    <h1>display: grid; // align-self: flex-center;</h1>
    <div class="grid container stretch">
      <div class="item align-self-center">1</div>
      <div class="item ">2</div>
      <div class="item ">3</div>
    </div>
  </div>
```
```css
  .streach {
    align-items: stretch;
    /* Estica os itens.*/
  }

  .align-self-start {
    align-self: start;
  }
  .align-self-end {
    align-self: end;
  }
  .align-self-center {
    align-self: center;
  }
  .align-self-stretch {
    align-self: stretch;
  }
```
