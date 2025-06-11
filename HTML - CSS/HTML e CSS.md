O curso
> [!Summary] Sumário
> - HTML e CSS para iniciantes
> 	FronEnd, HTML, Tags, Acessibilidade, CSS, Grid Layout, Flebox, Media Queries, Responsivo, VS Code e mais.
> - Pré-requisitos
> 	Totalmente do zero
> - Ferramentas
> 	Visual Studio Code

# Projetos
- Portifólio Simples:![[HTML - CSS/imagens/img-01.png]]
- Projeto Final:![[HTML - CSS/imagens/img-02.png]]
Além desses dois projetos grandes teremos alguns mini projetos.
>[!note] Grade
>- HTML e CSS para Iniciantes
>	HTML, CSS, JavaScript, Editor de Código e browser
>- CSS Posicionamento
>	Margin, Grid, Flexbox, Position
>- HTML e Semântica
>	Semântica e Acessibilidade, Pontos de Referência, Listas, Navegação.
>- CSS Propriedades
>	Unidades, Tipografia, Background, Pseudo Classes e Elementos
>- Responsivo
>	Media Queries, Grid, Object Fit e max Width
>- Projeto Portfólio
>	Projeto criado do zero
>- Ferramentas
>	Linha de Comando, Git e Automação
>- Mais HTML e CSS
>	Formulários, Especialidade, Propriedades Customizadas e CSS Utilitário
>- Projeto Final
>	Projeto Bikcraft Criado do Zero
>- JavaScript Básico
>	Tipos de dados, manipular o dom, objetos e outros
>- JavaScript Projeto
>	Link ativo, mostrar/esconder conteúdo, galeria de imagens, plugins e mais.
>- Produção
>	Domínio, Hospedagem, Servidor, Formulário
# HTML, CSS e JavaScript
## HTML
- HyperText Markup Language
	Linguagem de marcação de hipertexto
- Marcar o Conteúdo e define a estrutura do site
	Serve para marcarmos os textos(títulos, parágrafos, listas), adicionamos imagens, vídeos, links e mais. Dá sentido (Semântica) ao conteúdo.
- .html
	Arquivo de texto simples terminado em .html
	`<p>Olá Mundo</p>` (`<p>` tag de parágrafo).
## CSS 
- Cascading Style Sheets
	Folhas de estilo em cascata
- Define o estilo do documento
	Cor do Texto, Tamanho do texto, tamanho da imagem, posição do conteúdo, cor de fundo, sombras e mais
- .css
	Arquivo de texto simples terminado em .css
	`p{color: blue;}` (`p` e um **seletor** para atacarmos a tag `<p>`)
## JavaScript
- JavaScript
	Linguagem de script (programação)
- Altera o comportamento do documento
	Utiliza para modificar o estilo, criar galerias de imagens, observar as ações do usuário, puxar informações de outros sites, manipular dados e mais.
- .js
	Arquivo de texto simples terminado em .js
	``` js
	function mudar(){
		texto.style.color = 'blue';
	}
	texto.addEventListener('click', mudar)
	
	```
Esses três são o bloco principal de web:
- HTML marcou o texto.
- CSS deu a estilização.
- JavaScript modificou ele.
# Editor de código
- Editores
	Visual Studio Code, Sublime Text, Vim e outros.
- Vantagens
	Destaca Sintaxe, autocompleta o código, organiza o código, informa erros e mais.
# Browser
- Executa o código
	Responsável por executar e interpretar o código HTML, CSS e JavaScript 
- Diferentes browsers
	Chrome, Firefox, Safari, Edge, Opera e outros.
- Diferentes dispositivos
	Windows, Mac, Desktop, Mobile, Smart TV, e outros.
# Estrutura HTML
## Anatomia Tag
- Tag
	As tag's (etiquetas) servem para marcamos o conteúdo no HTML. Geralmente abrimos `<a>` e fechamos `</a>` após o conteúdo.
	[[Case insensitive]], mas e boa prática escrever com minúsculas `<html>`. 
- Atributo
	Os atributos dão informações extras sobre uma tag para o browser.
	[[Case insensitive]] o nome do atributo, [[Case sensitive]] o valor do atributo.
![[HTML - CSS/imagens/img-03.png]]
# Tag 
- Conteúdo
	As tags servem para inserirmos conteúdos como textos, imagens, vídeos e outros. Além da dar informações para o browser como o título do site, linguagem e outras.
- Semântica 
	Dar sentido ao conteúdo, a escrita de um documento semântico beneficia principalmente leitores de tela (acessibilidade) e leitores de códigos (robôs como o do Google).
- Interação com CSS e JavaScript
	Através das marcações das tags que conseguimos selecionar elementos para mudarmos o seu estilo ou comportamento.
## Tags comuns
- `p`
	marca um parágrafo
- `h1, h2, h3, h4, h5, h6`
	Marcamos diferentes níveis de títulos. 
- `a`
	Marca um link
``` html
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>

<body>
  <h1>Cursos Online de HTML e CSS</h1>
  
  <h2>HTML</h2>
  <p>Curso de HTML, aprenda do zero</p>
  <a href="/html">Curso de HTML</a>

  <h2>CSS</h2>
  <p>Curso de CSS, aprenda do zero</p>
  <a href="/css">Curso de CSS</a>

  <h2>JavaScript</h2>
  <p>Curso de JavaScript, aprenda do zero</p>
  <a href="/javascript">Curso de JavaScript</a>
</body>

</html>
```
## Estrutura simples de um HTML
``` html
<!DOCTYPE html>
<html lang="pt-br"> <!-- Definindo o idioma do documento como português do Brasil -->
<head> <!-- Cabeçalho do documento HTML -->
  <meta charset="UTF-8">  <!-- Normalização de caracteres com acento -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0"> <!-- Responsividade -->
  <title>Document</title> <!-- Título da aba do navegador -->
</head>
<body> <!-- Corpo do documento HTML -->
</body>
</html>
```
# Links
- link
	Cria uma relação entre um documento HTML e um arquivo CSS.
- rel
	Define o tipo de arquivo (stylesheet para CSS). É possível linkar outras também como favicons
- href
	Define o caminho do arquivo
	`<link rel="stylesheet" href="/style.css" />`
## caminho (path)
- Absoluto
	```html
	<a href="https://google.com.br">Google.com</a>  
	```
	Usado para arquivos externos ao nosso site
- Relativo
	```html
	<a href="nomeDoArquivo">Google.com</a>  
	```
	Usado para arquivos internos do nosso site
## Caminhos Relativos
- /index.html
	Arquivos index.html no diretório raiz `/`
- /produtos/bicicletas.html
	Arquivos bicicletas.html no diretório `/produtos` localizado na raiz
- index.html ou ./index.html
	Arquivos index.html no diretório atual `./`
- ../index.html
	Arquivos index.html um diretório anterior ao atual `../` 
- ../../index.html
	Arquivo index.html dois diretórios anteriores ao atual.
# CSS
## Anatomia CSS
- Seletor
	Seleciona o elemento(s) que deve ser estilizado.
- Bloco CSS
	Engloba as propriedades `{}` que serão aplicadas ao seletor
- Propriedade
	Define o que será alterado.
- Valor
	Define o valor do novo estilo.
![[HTML - CSS/imagens/img-04.png]]
``` css
h1{
  font-family: Arial, Helvetica, sans-serif;
  color: rgb(0, 30, 65); 
}
span{
  color: rgb(0, 89, 190); 
}

a{
  display: inline-block;
  font-size: 18px;
  text-decoration: none;
  font-family: Arial, Helvetica, sans-serif;
  color: rgb(0, 89, 190);
}
a::after{
  content: '';
  display: inline-block;
  width: 100%;
  height: 2px;
  margin-bottom: 10px;
  background-color: rgb(0, 89, 190);
}

a:hover{
  color: rgb(0, 51, 109);
}
a:hover::after{
  background-color: rgb(0, 51, 109);
}
```
## Seletores CSS
- h1, p (tag)
	A vírgula permite selecionarmos múltiplos elementos para a aplicação de um mesmo estilo
- p a (tag)
	Seleciona todos os `a` que tiverem dentro de `p` como e elemento pai (não precisa ser filho **Direto**).
![[HTML - CSS/imagens/img-05.png]]
### Id
Atributos HTML que adicionam um identificador **único** na tag. Esse identificador pode ser utilizado no CSS para selecionarmos o elemento: ``#nomeid``
![[HTML - CSS/imagens/img-06.png]]
### Class
classe em HTML adicionam um classificador que seleciona **várias** tags. Esse classificador pode ser utilizado no CSS para selecionarmos o elemento: ``.nomeclass``
![[HTML - CSS/imagens/img-07.png]]
# Background e Cores
 
## `background color:`
muda cor de fundo de um elemento.
```html
  <!-- mudadando a cor de fundo -->
   <h1>Front End</h1>
   <h2><a href="#">Origamid</a></h2>
```
``` css
h1{
  background-color: black;
  color: white;
}

a{
  display: inline-block;
  background-color: seagreen;
  color: white;
}
```

![[HTML - CSS/imagens/img-08.png]]
## Hexadecimal
- hexadecimal
	A cor é representada através de um  código de 6 caracteres que vão de 0 a F.
- `#84e` = `#8844ee`
```html
  <!-- mudadando a cor de fundo -->
   <h1>Front End</h1>
   <h2><a href="#">Origamid</a></h2>
```
```css
h1{
  background-color: #8844ee;
  color: #ffffff;
}

a{
  display: inline-block;
  background-color:#84e;
  color: #000;
  padding: 5px;
}
```
![[HTML - CSS/imagens/img-09.png]]
## RGBA
recebe três valores diferentes com cada valor indo de 0 a 255.
```html
  <!-- mudadando a cor de fundo -->
   <h1>Front End</h1>
   <h2><a href="#">Origamid</a></h2>
```
```css
h1{
  background-color: rgb(12, 0, 175);
  color: rgb(255, 255, 255);
}

a{
  display: inline-block;
  background-color:rgb(164, 126, 221);
  color: rgb(0, 0, 0);
  padding: 5px;
}
```
![[HTML - CSS/imagens/img-10.png]]
para saber mais sobre cores podemos acessar esse outro arquivo: [[UI e UX#Cores|Cores]]
# Box Model
> [!info] Índice
> - Content (conteúdo).
> Define a largura inicial da caixa (salvo elementos de bloco).
> - Padding (preenchimento).
> Separa o conteúdo das bordas da caixa. É a margem interna.
> - Border (borda).
> Define bordas para a caixa. 
> - Margin (margem).
> define a distância entre uma caixa e outra.
> - Width (largura).
> A largura total da caixa, por padrão é o somatório do conteúdo + padding (left/right) + border (left/right).
> - Height (altura).
> A altura total da caixa, por padrão é o somatório do conteúdo + padding (top/bottom) + border (top/bottom).

![[HTML - CSS/imagens/img-12.png]]
## Caixas
Uma interface web é composta de diversas caixas que organizam o conteúdo
![[HTML - CSS/imagens/img-11.png]]
## Pixel
- unidade de referência 
	É a unidade de referência da web, pois as telas são desenvolvidas em pixels.
- monitores
	Um monitor de: 3840(largura em px) X 2160(altura em px) = 8.294.400
- px em CSS 
	No CSS o pixel (px) é uma unidade de referência e não representa 1px exato do seu dispositivo (é adaptável em relação à densidade da tela.)
## div
A `<div>` é um elemento de bloco block genérico que serve para auxiliar no posicionamento dos elementos/conteúdo na tela.
Existem também elementos semânticos como main, section, nav e outros que veremos em outras aulas.
```html
  <div class="quadrado"></div>
  <h1>Front End</h1>
  <div class="quadrado">
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
  </div>
```
```css
.quadrado{
  display: inline-block;
  background: #aaa;
  width: 140px;
  height: 80px;
  border: 5px solid black;
  padding: 20px;
  margin: 20px;
}

h1{
  background: #84e;
  border: 5px solid black;
  padding: 20px;
  margin: 40px;
}
```
![[HTML - CSS/imagens/img-13.png]]
# Estilos do browser
- padrão
	Os browsers possuem um css inicial que é aplicado ao documento
- h1 vs p
	Por isso quando marcamos um h1 o texto fica maior/negrito em relação a um texto marcado como um p
![[img-14.png]]
# inherit (Herança)
Existem propriedades do CSS que são passadas do pai para o filho como uma herança (inherit).
- Exemplos
	color, font-size, font-family e outras.
- Padrão vs Herança 
	O valor padrão irá escrever por cima da herança. por isso ao definirmos uma color no body, os `<a>` não mudam de cor
![[HTML - CSS/imagens/img-15.png]]
```html
  <h1>Curso de HTML</h1>
  <p>Cusos de Design</p>
  <button>clique</button>
  <div>Cursos de CSS</div>
  <a href="#">Cursos de JavaScript</a>
```
```css
body{
  color: cadetblue;
}
```
`<button>` e `<a>` não estão herdando a cor do body porque no browser eles tem o valor padrão de `webkit-link`, e quando há um valor qualquer ele não herda, então se quisermos mudar o valor de `<a>` vamos ter que atacar ele direto mudando a cor dele, ou mudando-o para o valor de herança inherit
```html
  <h1>Curso de HTML</h1>
  <p>Cusos de Design</p>
  <button>clique</button>
  <div>Cursos de CSS</div>
  <a href="#">Cursos de JavaScript</a>
```
```css
body{
  color: cadetblue;
}
a{
	color: cadetblue;
}
/* ou */
a{
	color: inherit; /*herança*/
}
```
# Display
## Fluxo do layout
O fluxo do layout no HTML ocorre conforme o modo de escrita definido. Por padrão, de cima pra baixo, da esquerda para a direta.
- span
tag genérica que não possui nenhum estilo pré definido/Semântica. é equivalente a uma div, mas sem o display block.
```html
Texto direto no body <a href="#">Texto no link</a> <span>Texto no span</span>
Texto direto no body2 <a href="#">Texto no link2</a> <span>Texto no span2</span>
```
![[img-16.png]]
podemos mudar o fluxo dele:
```html
Texto direto no body <a href="#">Texto no link</a> <span>Texto no span</span>
Texto direto no body2 <a href="#">Texto no link2</a> <span>Texto no span2</span>
```
```css
body{
  writing-mode: vertical-lr;
}
```
![[HTML - CSS/imagens/img-17.png]]
## Display inline e block
Define como a caixa (box model) irã se comportar
- inline
	Respeita o fluxo da escrita sem iniciar uma nova linha, não é possível definir valores de `widht`, `height`, `margin(top/bottom)` e etc. É o estilo padrão
- block
	inicia uma nova linha e não permite que outros elementos sejam posicionados em sua linha, aceita todas as propriedades do box model. Estilo inicial de elementos como h1, p, div, e outros.
```html
  texto puro
  <div>Novo texto em div</div>
  <a href="#">Novo Link</a>
  <strong>Esse é um texto em negrito.</strong>
  <h1>Novo h1</h1>
  <span>Novo texto em span</span>
  <div>esse é um texto com
    <div>um elemento em bloco</div> dentro dele
  </div>
```
```css
div, a, h1, strong, p{
  border: 1px solid rgba(255, 0, 0, 0.281);
}
```
![[HTML - CSS/imagens/img-18.png]]
## none e inline-block
- none 
	Remove o elemento completamente da tela
- inline-block
	O elemento continua em linha mas parra a receber as propriedades do box model
```html
 <div class="esconder">Esse elemento será "apagado"</div>
 <div>
  acesse o meu <a href="#" class="link">link inline-block</a> aqui
 </div>

 <div>novo elemento de bloco</div>
 <div>
  acesse o meu <a href="#" class="link-2">link inline</a> aqui
 </div>
 <div>novo elemento de bloco</div>
```
```css
.esconder{
  display: none;
}

div > .link{
  display: inline-block;
  margin: 20px;
  width: 200px;
  height: 50px;
  background-color: aqua;
}

div > .link-2{
  display: inline;
  margin: 20px;
  width: 200px;
  height: 50px;
  padding: 10px;
  background-color: aqua;
}
```
![[img-19.png]]
# Image
`img`
A tag `img` é utilizada para adicionarmos imagens á nossa página.
- src
	Atributo que define o caminho da imagem (pode ser tanto pela internet quanto pelo computador local)
- alt
	Texto alternativo, caso a imagem não consiga aparecer. Ele também será lido por leitores de tela para melhorar a acessibilidade.
- max-width: 100%;
	Geralmente definimos um width máximo de 100% para a imagem, assim ela não cresce além do tamanho do elemento pai.
- display: block;
	usamos porque a img vem como padrão o display: inline-block; isso faz com que a img tenha um pequeno espaço para todos os lados.
```html
<img src="imgs/bryan-goff-f7YQo-eYHdM-unsplash.jpg" alt="Imagem da Galaxia">
```
```css
 img{
  max-width: 100%;
  display: block;
 }
```
![[HTML - CSS/imagens/img-20.jpg]]
>[!info] observação
>quando formos colocar uma imagem em nosso site temos que ter cuidado com a nossa resolução, uma coisa que devemos fazer e pegar uma imagem do dobro do tamanho e setar um tamanho por código pela metade, e.g. temos uma imagem de 200px, em um monitor normal ele ficaria nitida mas em um monitor de resolução maior tipo 4k ela ficaria borrada, para solucionar isso vamos pegar essa imagem e dobrar o tamanho dela, mas no código vamos colocar que ela terá 200px de largura, então ela ficará nitida para todos os monitores.
>Clique aqui para saber mais sobre a parte teórica: [[UI e UX#Imagens|Imagens]]

`svg` e `png`
Para usarmos o `svg` e `png` fazemos a mesma coisa, mas no final vamos colocar`.svg` e `.png`.
Para saber a diferença entre todos os tipos de imagens clique aqui: [[UI e UX#Imagens|Imagens]].
Quase nunca colocaremos em nosso site imagens de tamanho maior que 1mb. podemos otimizar essas imagens pelo site [Squoosh](https://squoosh.app/), também vamos otimizar a imagem pelo tamanho dela.
![[img-21.png]]
A imagem otimizada reduziu 73% do tamanho da image, poderíamos reduzir ainda mais caso abaixássemos a largura e a altura.
## Imagem dinâmica
A imagem dinâmica vai escolher imagens diferentes para cada tipo de tamanho de tela
![[img-92.png]]
![[img-93.png]]
![[img-94.png]]
```html
<picture>
    <source media="(max-width: 825px)" srcset="img/img-p.png" sizes="image/png">
    <source media="(max-width: 1125px)" srcset="img/img-m.png" sizes="image/png">
    <img src="img/img-g.png" alt="imagem grande">
  </picture>
```

# Posicionamento
## Top, Right, Bottom, Left
Propriedades como margin, padding, e border permitem definirmos valores diferentes para cada um dos lados da caixa(Box Model).
![[img-22.png]]
```html
  <span class="span-1"></span>
  <span class="span-2"></span>
  <span class="span-3"></span>
```
```css
span{
  display: inline-block;
  background-color: #ddd;
}

.span-1{
  padding: 30px;
}

.span-2{
  padding: 20px 40px;
}

.span-3{
  padding: 40px 100px 200px 10px;
}
```
![[img-23.png]]
# Grid
`grid`
Com o `display: grid;` é possível definirmos colunas e linhas para organizarmos os elementos que estiverem dentro do grid.
- `grid-template-columns`
	Define o total de colunas e o tamanho de cada uma.
- `fr`
	fr é uma unidade fracionária que terá como objetivo distribuir o espaço restante entre os elementos do grid. 
- `gap`
	Cria uma distância entre os elementos do grid, tanto horizontal quanto vertical.
## Align e Justify Content
guia CSS grid Layout
- [CSS Grid Layout](https://www.origamid.com/projetos/grid/)
O Align e Justify Content servem para distribuir colunas dentro do grid. para as duas propriedades temos: 
- `start(inicio)`
```html
  <h1>Comércio Eletrônico</h1>
  <div class="container-grid">
    <div class="container-inside">
      <h2>Camisa</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
    <div class="container-inside">
      <h2>Bermuda</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
    <div class="container-inside">
      <h2>Short</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
    <div class="container-inside">
      <h2>Saia</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
  </div>
```
```css
body{
  font-family: Arial, Helvetica, sans-serif;
}

h1{
  text-align: center;
}

.container-grid{
  display: grid;
  grid-template-columns: 300px 300px;
  gap: 5px;
  justify-content: start; /* Início */
}

.container-inside{
  border: 1px solid rgb(168, 168, 168);
  padding: 5px;
}
.container-inside h2{
  font-size: 20px;
  font-weight: bold;
}
.container-inside a{
  background-color: #a8f;
  color: #103;
  padding: 10px 20px;
  display: block;
  text-decoration: none;
  border-radius: 4px;
}
```
![[img-24.png]]
- `center(centro)`
```html
  <h1>Comércio Eletrônico</h1>
  <div class="container-grid">
    <div class="container-inside">
      <h2>Camisa</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
    <div class="container-inside">
      <h2>Bermuda</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
    <div class="container-inside">
      <h2>Short</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
    <div class="container-inside">
      <h2>Saia</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
  </div>
```
```css
body{
  font-family: Arial, Helvetica, sans-serif;
}

h1{
  text-align: center;
}

.container-grid{
  display: grid;
  grid-template-columns: 300px 300px;
  gap: 5px;
  justify-content: center; /* Centro */
}

.container-inside{
  border: 1px solid rgb(168, 168, 168);
  padding: 5px;
}
.container-inside h2{
  font-size: 20px;
  font-weight: bold;
}
.container-inside a{
  background-color: #a8f;
  color: #103;
  padding: 10px 20px;
  display: block;
  text-decoration: none;
  border-radius: 4px;
}
```
![[img-25.png]]
- `end(fim)`
```html
  <h1>Comércio Eletrônico</h1>
  <div class="container-grid">
    <div class="container-inside">
      <h2>Camisa</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
    <div class="container-inside">
      <h2>Bermuda</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
    <div class="container-inside">
      <h2>Short</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
    <div class="container-inside">
      <h2>Saia</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
  </div>
```
```css
body{
  font-family: Arial, Helvetica, sans-serif;
}

h1{
  text-align: center;
}

.container-grid{
  display: grid;
  grid-template-columns: 300px 300px;
  gap: 5px;
  justify-content: end; /* Fim */
}

.container-inside{
  border: 1px solid rgb(168, 168, 168);
  padding: 5px;
}
.container-inside h2{
  font-size: 20px;
  font-weight: bold;
}
.container-inside a{
  background-color: #a8f;
  color: #103;
  padding: 10px 20px;
  display: block;
  text-decoration: none;
  border-radius: 4px;
}
```
![[img-26.png]]
- `stretch(aumenta o item (padrão))`
```html
  <h1>Comércio Eletrônico</h1>
  <div class="container-grid">
    <div class="container-inside">
      <h2>Camisa</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
    <div class="container-inside">
      <h2>Bermuda</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
    <div class="container-inside">
      <h2>Short</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
    <div class="container-inside">
      <h2>Saia</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
  </div>
```
```css
body{
  font-family: Arial, Helvetica, sans-serif;
}

h1{
  text-align: center;
}

.container-grid{
  display: grid;
  grid-template-columns: 300px 300px;
  gap: 5px;
  justify-content: stretch; /* Padrão */
}

.container-inside{
  border: 1px solid rgb(168, 168, 168);
  padding: 5px;
}
.container-inside h2{
  font-size: 20px;
  font-weight: bold;
}
.container-inside a{
  background-color: #a8f;
  color: #103;
  padding: 10px 20px;
  display: block;
  text-decoration: none;
  border-radius: 4px;
}
```
![[img-27.png]]
- `space-between(espaçamento entre os itens)`
```html
  <h1>Comércio Eletrônico</h1>
  <div class="container-grid">
    <div class="container-inside">
      <h2>Camisa</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
    <div class="container-inside">
      <h2>Bermuda</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
    <div class="container-inside">
      <h2>Short</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
    <div class="container-inside">
      <h2>Saia</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
  </div>
```
```css
body{
  font-family: Arial, Helvetica, sans-serif;
}

h1{
  text-align: center;
}

.container-grid{
  display: grid;
  grid-template-columns: 300px 300px;
  gap: 5px;
  justify-content: space-between; /* Entre */
}

.container-inside{
  border: 1px solid rgb(168, 168, 168);
  padding: 5px;
}
.container-inside h2{
  font-size: 20px;
  font-weight: bold;
}
.container-inside a{
  background-color: #a8f;
  color: #103;
  padding: 10px 20px;
  display: block;
  text-decoration: none;
  border-radius: 4px;
}
```
![[img-29.png]]
- `space-around(espaçamento entre os itens e acima do primeiro e abaixo do último)`
```html
  <h1>Comércio Eletrônico</h1>
  <div class="container-grid">
    <div class="container-inside">
      <h2>Camisa</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
    <div class="container-inside">
      <h2>Bermuda</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
    <div class="container-inside">
      <h2>Short</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
    <div class="container-inside">
      <h2>Saia</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
  </div>
```
```css
body{
  font-family: Arial, Helvetica, sans-serif;
}

h1{
  text-align: center;
}

.container-grid{
  display: grid;
  grid-template-columns: 300px 300px;
  gap: 5px;
  justify-content: space-around; /* Entre, Antes e Depois */
}

.container-inside{
  border: 1px solid rgb(168, 168, 168);
  padding: 5px;
}
.container-inside h2{
  font-size: 20px;
  font-weight: bold;
}
.container-inside a{
  background-color: #a8f;
  color: #103;
  padding: 10px 20px;
  display: block;
  text-decoration: none;
  border-radius: 4px;
}
```
![[img-28.png]]
- `space-evenly(espaçamento igual entre todos os itens)`
```html
  <h1>Comércio Eletrônico</h1>
  <div class="container-grid">
    <div class="container-inside">
      <h2>Camisa</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
    <div class="container-inside">
      <h2>Bermuda</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
    <div class="container-inside">
      <h2>Short</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
    <div class="container-inside">
      <h2>Saia</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
  </div>
```
```css
/* start */
body{
  font-family: Arial, Helvetica, sans-serif;
}

h1{
  text-align: center;
}

.container-grid{
  display: grid;
  grid-template-columns: 300px 300px;
  gap: 5px;
  justify-content: space-evenly; /* Entre, Antes e Depois mais distibuido */ 
}

.container-inside{
  border: 1px solid rgb(168, 168, 168);
  padding: 5px;
}
.container-inside h2{
  font-size: 20px;
  font-weight: bold;
}
.container-inside a{
  background-color: #a8f;
  color: #103;
  padding: 10px 20px;
  display: block;
  text-decoration: none;
  border-radius: 4px;
}
```
![[img-30.png]]
A diferença entre o align e o justify e que o align e na vertical e o justify e na horizontal.
>[!info] observação
>Como o fr é uma unidade fracionária que tem como objetivo distribuir o espaço, então se utilizarmos ele para criar colunas o justify não dará resultado nenhum porque ele precisa de espaço para funcionar.

No `grid-template-columns` o valor padrão e auto, o auto ele vai aumentar até o conteúdo:
```html
  <h1>Comércio Eletrônico</h1>
  <div class="container-grid">
    <div class="container-inside">
      <h2>Camisa</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
    <div class="container-inside">
      <h2>Bermuda</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
    <div class="container-inside">
      <h2>Short</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
    <div class="container-inside">
      <h2>Saia</h2>
      <p>R$ 39</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a href="#">Comprar</a>
    </div>
  </div>
```
```css
/* start */
body{
  font-family: Arial, Helvetica, sans-serif;
}

h1{
  text-align: center;
}

.container-grid{
  display: grid;
  grid-template-columns: auto auto;
  gap: 5px;
  justify-content: space-evenly; /* Entre, Antes e Depois mais distibuido */ 
}

.container-inside{
  border: 1px solid rgb(168, 168, 168);
  padding: 5px;
}
.container-inside h2{
  font-size: 20px;
  font-weight: bold;
}
.container-inside a{
  background-color: #a8f;
  color: #103;
  padding: 10px 20px;
  display: block;
  text-decoration: none;
  border-radius: 4px;
}
```
![[img-31.png]]
na primeira coluna o texto das duas caixas e maior que as duas caixas da segunda coluna.
## place content
O place e apenas um atalho para as duas propriedades, se for apenas um valor por exemplo:
`place-content: start;`
ele vai aplicar tanto em justify quanto no align.
Mas se for dois valores, o primeiro valor será aplicado no align, e o segundo para o justify
`place-content: start end;`
## Grid Column
Usamos o grid column para expandir ou mudar um item de uma coluna, nessa imagem estamos usando o grid normalmente sem usar o grid column.
![[img-32.png]]
Agora estamos usando o grid column.
![[img-33.png]]
Para usar o grid column devemos atacar um item onde o pai tem um grid:
```html
    <div class="grid"> <!-- O Pai tem um grid -->
      <h1 class="titulo">Camisa</h1>
      <p class="preco">R$ 39</p>
      <img src="../05-images/imgs/bryan-goff-f7YQo-eYHdM-unsplash.jpg" alt="galaxia"> <!-- O Filho que vamos atacar com um grid column -->
      <p class="descricao">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quo, nam nihil commodi exercitationem unde necessitatibus possimus cum aliquam aliquid sint culpa at explicabo labore, esse nesciunt, natus facilis deserunt! Laboriosam.</p>
      <a class="comprar" href="#">Comprar</a>
    </div>
```
```css
.grid{
  display: grid;
  gap: 10px;
  grid-template-columns: 1fr 1fr;
}

img{
  grid-column: 2; /* O grid esta indo da 2 coluna ate a última */
}
```
![[img-34.png]]
Nos números acima podemos ver dois números principais, um número na vertical e outro na horizontal.
O numero na Vertical conta quantas linhas (3) há e o na Horizontal marca a quantidade de colunas (4).
Com uma `/` estamos falando em expansão, por exemplo vamos expandir essa imagem da linha 1 a 3.
![[img-35.png]]
```css
.grid{
  display: grid;
  gap: 10px;
  grid-template-columns: 1fr 1fr;
}

img{
  grid-column: 1/3;
}
```
- `1/-1`
Supomos que não sabemos quantas linhas nosso grid tenha mas queremos que ele fique sempre expandido em todas as colunas como fazer?
Para isso podemos utilizar o 1/-1.
```css
.grid{
  display: grid;
  gap: 10px;
  grid-template-columns: 1fr 1fr;
}

img{
  grid-column: 1/-1;
}
```
- `span`
O span vai servir para expandir a coluna de onde ele nasceu.
![[img-36.png]]
```css
.grid{
  display: grid;
  gap: 10px;
  grid-template-columns: 1fr 1fr 1fr 1fr;
}

img{
  grid-column: span 2;
}
```
Aqui temos 4 colunas e 5 itens, mas como expandimos a imagem em 2 colunas, ela vai ocupar 2 colunas do lugar que ela nasceu e vai empurrar os itens que vem depois dela.
## Aling e Justify items
### align items e justify items
- align-items: start | center | end | stretch
	Alinha os items na horizontal.
- justfy-items: start | center | end | stretch
	Alinha os items na vertical.
- place-items: align e justify
	atalho para align e justify.
![[img-37.png]]
```css
.grid{
  display: grid;
  gap: 10px;
  grid-template-columns: 1fr 1fr ;
  align-items: center; 
}

img{
  grid-column: span 2;
}
```
>[!info] observação
>- Setamos esse valor direto no elemento pai, então ele afetará todos os itens que estão dentro desse container.
>- Assim como no content que precisamos de espaços para mover os items aqui também funciona da mesma maneira.
### Aling Justify self
Para utilizar esse alinhamento em 1 item apenas utilizamos o `aling/justfy-self`
Agora sim vamos atacar os filhos e não o pai.
![[img-38.png]]
```css
.grid{
  display: grid;
  gap: 10px;
  grid-template-columns: 1fr 1fr ;
}

.titulo{
  grid-column: 2;
}

.preco{
  place-self: start end;
}
```
>[!info] observação
>Para alinharmos o texto e com text-aling, se tentarmos utilizar o align, justify ou content vai dá errado, essas propriedades são feitas para alinhar o bloco do conteúdo e não o conteúdo em si.
## grid-template-rows
- grid-template-rows: 100px auto;
	Define o tamanho das linhas.
- grid-auto-rows
	Linhas são adicionadas automaticamente com o valor auto
- grid-row: 2
	Define a linha do item, funciona da mesma maneira que o grid-column
![[img-39.png]]
```css
.grid{
  display: grid;
  gap: 10px;
  grid-template-columns: 2fr 1fr ;
  grid-template-rows: 300px; /*cria novas linhas*/
  grid-auto-rows: 200px; /*Todas as linhas geradas automaticamente terão 200px*/
}
```
### grid row
Funciona igual o grid column mas com linhas
![[img-41.png]]
```css

.grid{
  display: grid;
  gap: 10px;
  grid-template-columns: repeat(2, 1fr);
}

.preco{
  grid-row: 3;
}
```
### grid area
Junta o grid column com o grid row:
![[img-42.png]]
```css

.grid{
  display: grid;
  gap: 10px;
  grid-template-columns: repeat(2, 1fr);
}

.preco{
  /* grid-row: 2;
  grid-column: 2; */
  grid-area: 2/2;  
}
```
### repeat()
Se repetirmos muitos valores podemos usar o repeat, invés de colocarmos  1fr 1fr 1fr 1fr, podemos usar:
![[img-40.png]]
```css
.grid{
  display: grid;
  gap: 10px;
  grid-template-columns: repeat(5, 1fr);
}
```
onde no primeiro valor será usado para a quantidade de vezes que ele irá repetir e o segundo valor será para qual valor será usado (nesse caso 1fr).
# Flexbox
- display: flex;
	Os filhos passa a ter um tamanho flexível e ficam um ao lado do outro.
- flex-wrap: wrap;
	Caso não caiba todos os elementos em uma mesa linha quebre para a próxima.
- gap
	Define uma distância entre os elementos.
![[img-43.png]]
```css
.flex{
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
  justify-content: center;
}

h2{
  background-color: #e7e7e7;
  border: 1px solid #ccc;
  padding: 10px;
}
```
## flex
- flex-grow: 1;
	Fala se esses elementos devem crescer para ocupar o espaço vazio. o `0` impede o crescimento, valores maiores que `0` funcionam como unidade `fr` do css grid.
![[img-44.png]]
```css
.flex{
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
}

h2{
  background-color: #e7e7e7;
  border: 1px solid #ccc;
  padding: 10px;
  flex-grow: 1;
}
```
- flex-basis: 200px;
	Valor inicial antes de distribuir o espaço em branco.
![[img-45.png]]
```css
.flex{
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
}

h2{
  background-color: #e7e7e7;
  border: 1px solid #ccc;
  padding: 10px;
  flex-grow: 1;
  flex-basis: 0; /* Todos estão com o tamanho igual, independente do conteúdo interno*/
}
```
- flex-shrink: 0;
	Caso exista um valor de base, o flex-shrink irá determinar se esse valor pode ser reduzido ou não. `0` significa que ele não pode ser reduzido
![[img-46.png]]
```css
.flex{
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
}

h2{
  background-color: #e7e7e7;
  border: 1px solid #ccc;
  padding: 10px;
  flex-grow: 1;
  flex-basis: auto;
  flex-shrink: 1; /* Vai quebrar o conteudo para não estourar a caixa */
  flex-shrink: 0; /* Vai estourar a caixa mas não vai quebrar o conteudo */
}
```
- flex: 1; 
	Atalho para `flex-grow: 1;` `flex-shrink: 1;` e `flex-basis: 0;`
Geralmente usaremos somente o flex: 1;
# Flex vs Grid
Use ambos no seu layout, eles resolvem problemas diferentes. O grid te dá controle em todos os eixos e o flexbox no total de itens por linha.
![[img-47.png]]
```css
.flex{
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
  border: 1px solid #ccc;
  padding: 10px;
}

h2{
  background-color: #e7e7e7;
  border: 1px solid #ccc;
  padding: 10px;

}

.grid{
  display: grid;
  gap: 10px;
  grid-template-columns:1fr 1fr;
  border: 1px solid #ccc;
  padding: 10px;
  margin-top: 50px;
}

h1{
  grid-column: 1/-1;
}
```
# Position
A propriedade position possui valores que remove o elemento do fluxo padrão do documento. O padrão é o valor `static`
- `position: fixed;`
	Fixa o elemento na tela
- `top`, `right`, `left` e `bottom`
	Define o posicionamento dos elementos que não estão no fluxo padrão.
![[img-48.png]]
```html
  <h1>1° conteúdo</h1>
  <h1>2° conteúdo</h1>
  <h1>3° conteúdo</h1>
  <div class="fixed">
    <p>Neste site usamos crack</p>
  </div>
```
```css
h1 {
  border: 2px solid #ccc;
  padding: 20px 20px 400px 20px;
}

p{
  background: #e6e6e6;
  border: 1px solid #000;
  padding: 20px;	
  margin: 0;
  font-size: 20px;
}

.fixed{
  position: fixed;
  top: 20px;
  left: 20px;
  right: 20px;
}
```
- `position: relative;`
	É relativo ao seu local de nascimento. Mesmo mudando de local ele continua ocupando o espaço de início, e o bloco que está se movendo não ocupa espaço nenhum
- - `top`, `right`, `left` e `bottom`
	Define o posicionamento dos elementos que não estão no fluxo padrão.
![[img-49.png]]
```css
/* Relative */
.content-1, .content-2{
  background: #f0f0f0;
  border: 1px solid #000;
  padding: 20px;	
  margin-top: 40px;
  font-size: 20px;
}

span{
  background: #969696;
  border: 1px solid #000;
  padding: 5px 10px;	
  margin: 0;
  font-size: 20px;
  position: relative;
  top: 150px; /* Está a 150px de onde ele nasceu*/
}
```
- `position: absolute;`
	Para de ocupar lugar no flow do layout, podendo ficar acima dos elementos da tela, quando utilizamos um `top:0;` por exemplo eles ficarão um em cima do outro e relativo a tela.
![[img-50.png]]
```css
/* Absolute */
.content-1, .content-2{
  background: #f0f0f0;
  border: 1px solid #000;
  padding: 20px;	
  margin-top: 40px;
  font-size: 20px;
}

span{
  background: #969696;
  border: 1px solid #000;
  padding: 5px 10px;	
  margin: 0;
  font-size: 20px;
  position: absolute;
  top: 400px;
}
```
- `position: absolute;` + `position: relative;` 
	Usando o position relative em um pai e absolute em um filho, o filho se posicionará dentro do pai
![[img-51.png]]
```html
<div class="content-1">
    <h1>container PAI</h1>
    <div class="content-2">
      <h1>container FILHO</h1>
    </div>
</div>
```
```css
.content-1{
  width: 800px;
  height: 800px;
  background: #f0f0f0;
  border: 1px solid #000;
  padding: 20px;	
  margin: auto;
  margin-top: 40px;
  font-size: 20px;
  position: relative;

}
.content-2{
  background: #f0f0f0;
  border: 1px solid #000;
  padding: 20px;	
  margin-top: 40px;
  font-size: 20px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

```
- `z-index`
	Muda o eixo de Profundidade
![[img-52.png]]
```css
.content-1{
  width: 800px;
  height: 400px;
  background: #f0f0f0;
  border: 1px solid #000;
  padding: 20px;	
  margin: auto;
  margin-top: 40px;
  font-size: 20px;
  position: relative;

}
.content-2{
  background: #f0f0f0;
  border: 1px solid #000;
  padding: 20px;	
  margin-top: 40px;
  font-size: 20px;
  position: absolute;
  top: 90%;
  z-index: -1;
}

```
# Semântica
Por qual motivo realmente devemos marcar o HTML com tags semânticas (h1, main...) e não apenas com tags genéricas (div, span...)
- Acessibilidade
	Leitores de tela (JAWS, NVDA, VoiceOver) Utilizam as tags para a navegação e compreensão do conteúdo. Interfaces de voz estão cada vez mais presentes.
- Browsers e Funcionalidades
	Define um estilo padrão para o conteúdo, mesmo sem o CSS. Facilita a organização do conteúdo em browsers que oferecem modo leitura.
- Indexadores e máquina
	Facilita o trabalho de indexadores como o robô do Google a identificar o conteúdo do seu site. (Expeculação)
Imagem com tags semânticas
![[img-53.png]]
Imagem sem tags semânticas
![[img-54.png]]
A semântica afeta tanto pessoas com dificuldades quanto os normais, na segunda imagem não como saber o que é um titulo principal, secundário ou texto normal.
# Pontos de referência
## Landmarks
Tags que marcam pontos de referência (Landmarks) foram introduzidos no lançamento do HTML5. Antes era utilizado o atributo role.
Visualmente o efeito que essas tags possuem é similar ao das div's, elas não muda em nada o conteúdo/apresentação. (section altera os headers)
>[!note]
>`<main>`
>`<nav>`
>`<section>`
>`<article>`
>`<aside>`
>`<footer>`
>`<header>`
## main
A tag `<main>` marca o conteúdo principal da página.
- Exemplos:
	Blog: conteúdo do artigo. Comércio eletrônico: descrição/imagem/preço do produto.
- Observação
	Utilize 1 por página
![[img-55.png]]
```html
<main>
    <h1>Ninbus Stark</h1>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Facere odit exercitationem earum quo soluta dolore hic quos, omnis, obcaecati totam voluptatibus blanditiis ex, qui repellendus tempora? Numquam eos minus velit!</p>
  </main>
```
## Navegação
a tag `<nav>` marca um bloco de navegação.
- Exemplos:
	Geralmente utilizado para a navegação primária e secundária do site.
- Observação
	Evite o uso de diversas tags `<nav>`, use apenas para navegações essenciais.
![[img-56.png]]
```html
 <!-- NAV -->
   <nav aria-label="primaria"> 
    <ul>
      <li><a href="#">item1</a></li>
      <li><a href="#">item2</a></li>
      <li><a href="#">item3</a></li>
      <li><a href="#">item4</a></li>
      <li><a href="#">item5</a></li>
    </ul>
   </nav>
```
> [!info] observação 
> aria-label dá uma etiqueta para a tag, isso vai fazer que em alguns leitores de tela apareça o nome 'primaria' junto de 'navegação' no leitor de tela. O aria-label e usado quando há varias tags nav no seu site.
## Article
A tag `<article>` representa uma região do site que é autoexplicativa (não precisa do restante do site para fazer sentido). Geralmente deve conter um título (h's).
- Exemplos
	Lista de produtos do site, um artigo, post na rede social e outros.
- aria-label
	Título da região visualmente escondido, mas lido pelo leitor de tela.
- aria-labelledby
	Caso o título exista na tela, marque o mesmo com um `id` e use este atributo para criar uma relação entre eles.
- observação
	Oficialmente não cria landmarks, mas muitos leitores de tela utilizam ela como referência para marcar regiões do site. A tag é até mais consistente do que a section para marcar regiões no site.
![[img-57.png]]
```html
<!-- Article -->
  <article aria-label="livros">
    <p>O Senhor dos Anéis</p>
    <p>O Hobbit</p>
  </article>

  <article aria-labelledby="celtitulo">
    <h2 id="celtitulo">Celulares</h2>
    <p>Conheça mais as marcas que vendemos no site</p>
  </article>
```
## Section
A tag `<section>` pode ser utilizada para agrupar o conteúdo do site em diferentes regiões. Geralmente o conteúdo necessita do seu contexto para ser compreendido.
- aria-label
	Se utilizada com o atributo `aria-label` cria uma região no site.
- observação
	o h1 é impactado em termos visuais quando utilizado na section. O section foi criado para melhor lidar com os headings, porém a sua idealização nunca foi implementada (até hoje 2021).
```html
<!-- SECTION -->
   <section>
    <h2>Sobre a surfbot</h2>
    <p>A empresa foi fudade em 2014</p>
   </section>
```
## Aside
A tag `<aside>` é utilizada para marcar o conteúdo complementar ao principal do site.
- Exemplos 
	Lista de post mais vistos, informações extras como a descrição de um termo usado em um artigo e mais.
```html
<!-- ASIDE -->
  <aside>
    <h3>Posts Relacionados</h3>
    <a href="#">Como aprender CSS</a>
    <a href="#">Como aprender HTML</a>
  </aside>
```
## Header
A tag `<header>` marca o cabeçalho do site (banner), onde geralmente estão presentes a marca, navegação do site e a vezes uma informação introdutória.
- Exemplos
	Pode também ser utilizada para marcar o cabeçalho de regiões como o título de um artigo, data, autor e outras informações.
- observação
	Apenas cria uma landmark se não estiver dentro de main, section, article ou aside.
```html
<!-- HEADER -->
  <header>
    <img src="" alt="">
    <nav>
      <a href=""></a>
      <a href=""></a>
    </nav>
  </header>
```
## Footer
É a mesma coisa do header.
# Listas
## ul
A tag `<ul>` marca uma lista de itens sem ordem (unordered list). Cada item da lista deve ser marcado com uma lista `<li></li>`.
- Acessibilidade
	Listas são anuncias pelo leitor de tela e o usuário é informado previamente de quantos itens existem na lista.
![[img-58.png]]
```html
  <h1>Listas Desordenadas</h1>
  <h2>Livros Recomendados</h2>
  <ul>
    <li>O Senhor dos Anéis</li>
    <li>O Hobbit</li>
    <li>Harry Potter</li>
    <li>Interestelar</li>
    <li>Um sonho de liberdade</li>
  </ul>
  <h2>Listas dentro de listas</h2>
  <ul>
    <li>Músicas Rápidas</li>
    <ul>
      <li>Timelapse</li>
      <li>November</li>
      <li>Na Mara</li>
      <li>Choros</li>
      <li>Infra 5</li>
    </ul>
    <li>Músicas Lentas</li>
    <ul>
      <li>Fish in the pool</li>
      <li>Pieces</li>
      <li>Deeply</li>
      <li>Silence</li>
      <li>Rise</li>
    </ul>
  </ul>
```
## ol
A tag `<ol>` marca uma lista de itens com ordem (ordered list). Cada item da lista deve ser marcado com uma lista `<li></li>`.
- Acessibilidade
	Listas são anuncias pelo leitor de tela e o usuário é informado previamente de quantos itens existem na lista.
![[img-59.png]]
```html
  <h1>Listas Ordenadas</h1>
  <h2>Livros Recomendados</h2>
  <ol>
    <li>O Senhor dos Anéis</li>
    <li>O Hobbit</li>
    <li>Harry Potter</li>
    <li>Interestelar</li>
    <li>Um sonho de liberdade</li>
  </ol>
  <h2>Listas dentro de listas</h2>
  <ol>
    <li>Músicas Rápidas</li>
    <ol>
      <li>Timelapse</li>
      <li>November</li>
      <li>Na Mara</li>
      <li>Choros</li>
      <li>Infra 5</li>
    </ol>
    <li>Músicas Lentas</li>
    <ol>
      <li>Fish in the pool</li>
      <li>Pieces</li>
      <li>Deeply</li>
      <li>Silence</li>
      <li>Rise</li>
    </ol>
  </ol>
```
## dl
A tag `<dl>` marca uma lista de definição (definition list). Cada item da lista deve ser marcado com um `<dt></dt>` para definir e um `<dd></dd>` para a definição do termo.
- Acessibilidade
	Listas são anuncias pelo leitor de tela e o usuário é informado previamente de quantos itens existem na lista.
![[img-60.png]]
```html
  <h1>Lista de Definição</h1>
  <h2>Perguntas frequentes</h2>
  <dl>
    <dt>Quais os meios de pagamento</dt>
    <dd>Dinheito, Pix e Cartão</dd>
    <dt>Emite Certificados</dt>
    <dd>Sim, emitimos para todos os cursos</dd>
  </dl>
```
# Navegação
O uso mais comum de listas é na marcação de blocos de navegação, pois um menu é uma lista de links.
![[img-61.png]]
```html
  <nav aria-label="primária">
    <ul>
    <li><a href="#">Sobre</a></li>
    <li><a href="#">Produtos</a></li>
    <li><a href="#">Contato</a></li>
    </ul>
  </nav>
```
```css
*{
  margin: 0;
  padding: 0;
}

nav > ul{
  display: flex;
  gap: 20px;
  margin: 40px;
}

nav > ul > li{
  list-style-type: none;
}


nav > ul > li > a{
  text-decoration: none;
  color: black;
  padding: 15px 30px;
  border: 1px solid rgb(201, 201, 201);
  border-radius: 5px;
}
```
## Sem Listas
Não é obrigatório o uso de listas para criar uma navegação.
Uma discussão sobre o assunto gerou os pontos positivos e negativos do uso sem listas, a conclusão foi de que com listas seria o ideal.
# Tags Semânticas
>[!note] Tags
>`<blockquote>`
>`<q>`
>`<cite>`
>`<em>`
>`<strong>`
>

![[img-62.png]]
```html
<h3>Blockquote</h3>
  <blockquote cite="https://professor.luzerna.ifc.edu.br/david-jose/2020/11/12/discurso-sobre-o-dinheiro-de-francisco-danconia-em-a-revolta-de-atlas-de-ayn-rand/">
    <p>“No Discurso do Dinheiro, Francisco d’Conia denuncia como o dinheiro se tornou o novo ídolo da humanidade, corrompendo valores, desumanizando relações e iludindo com uma falsa liberdade, enquanto aprisiona o ser humano à lógica do consumo e do poder.”</p>
  </blockquote>
  <p>Francisco d’Conia</p>
  <!--`<blockquote>` Marca uma citação extensa e recekbe um atributo cite com a fonte-->

  <h3>q</h3>
  <p>Como já dizia o poeta <q>se HTML está difícil, nem comece com JavaScript.</q></p>
  <!-- `<q>` Marca uma citação inline(no texto). -->

  <h3>cite</h3>
  <p>Eu indico o livro <cite>A Revolta de Atlas</cite> escrito por Ayn Rand. </p>
  <!-- Cite é utilizado pra citar o nome de um trabalho, livro, filme, peça ou algo parecido, Não e para citar o autor. -->

  <h3>em</h3>
  <p><em>Nenhum animal</em> foi maltratado na produção deste conteúdo. </p>
  <!-- `<em>` é utilizada para dar enfase em uma frase/palavra no texto. -->

  <h3>strong</h3>
  <p>É importante entender como os frameworks funcionam. Porém <strong>é essencial aprender JavaScript.</strong></p>
  <!-- `<strong>` é utilizada para arcar uma parte importante do conteúdo. -->
```
>[!info] Observação
>Essas tags são feitas para dá mais sentido em alguma parte do texto e não para decorar, se quisermos inserir textos em itálico, negrito ou outros, usamos o CSS
# Unidades
## rem
Unidade relativa ao tamanho da fonte no elemento raiz `html`. Na maioria dos browsers com configuração padrão `1rem = 16px`.
![[img-63.png]]
```css
.container p, .container a{
  margin: 20px 0;
  background-color: aqua;
  display: inline-block;
  padding: 15px 30px;
}

.container a{
  color: white;
  background-color: blue;
}

.px{
  font-size: 24px;
}

.rem{
  font-size: 1.5rem;
}
```
>[!info] Observação
> Porque não utilizamos o px direto? Vamos supor que alguém com dificuldade de leitura resolva aumentar o tamanho da fonte na raiz do browser, se o seu site usar `rem` que é calculado na raiz do browser, todo o seu site aumentará automaticamente, mas se ele for em `px` que é uma unidade fixa ele continuará do mesmo tamanho, então por questão de acessibilidade usamos o `rem`.
## vh e vw
`vh` representa o tamanho da altura da tela visível (viewport height) e `vw` da largura (viewport width). `100vw = 100% da tela` e  `100vh = 100% da altura tela`
- observação
	Antes do vh só existia a porcentagem, A porcentagem é problemática para definir o height, pois: height: 100%; significa 100% da altura do pai. A altura do pai sempre é definida pelo tamanho do conteúdo, então basicamente 100% de height não muda em nada
	`100vh` será sempre 100% da altura da tela, independente da quantidade de conteúdo 
![[img-64.png]]
```css
.div{
  width: 100vw; 
  height: 50vh; 
  background-color: aqua;
}
```
A imagem acima está ocupando 50vh ou seja 50% da altura da tela.
![[img-65.png]]
```css
section{
 width: 50%;
 height: 50vh;
 background-color: aquamarine; 
}
section div{
  width: 50%; /*como aqui é porcentagem ele está a 50% do tamanho do pai*/
  height: 100vh; /*como aqui é vh ele estoura o tamanho do pai*/
  background-color: cadetblue;
}
```
Aqui fizemos um exemplo para demonstrar que porcentagem`%` e diferente de viewport height`vh` a `%` sempre vai ser em relação ao pai, enquanto que `vh` será sempre em relação ao tamanho da tela. Na imagem acima o width está a 50% do pai dele (é está respeitando), ja o height está á 100vh (é está estourando o tamanho do pai).
## Calc
`calc()` é uma função de css que retorna um valor com base no cálculo efetuado entre os `()`. podemos combinar unidades.
- calc(100vw/3)
	representa 33% da tela
- calc(100% - 20px)
	Remove 20px de 100%
![[img-66.png]]
```css
div{
  background-color: cadetblue;
  width: calc(100vw - 100px);
  height: 100vh;
}
```
# Tipografia
Para acessar a parte teórica clique aqui: [[UI e UX#Tipografia|Tipografia]]
Existem diversas propriedades diferentes para ajustarmos a tipografia do site.
Geralmente começam com font ou text.
![[img-67.png]]
```css
p{
  font-size: 2rem; /* Tamanho da fonte */
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif; /* Familia da fonte */
  font-weight: 100; /* Peso da fonte */
  font-style: italic; /* Estilo da fonte */
  line-height: 1.5; /* Tamanho da linha */
  text-decoration: dotted; /* Decoração do texto */ 
  text-transform: capitalize; /* Tranforma o texto */
  text-indent: 50px; /* Identa o texto */
  text-align: justify; /* Alinhamento de texto */
  text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.397); /* Sombra em texto (Não use) */
  letter-spacing: 3px; /* Espaçamento entre as letras */
}
```
# Background
O background pode receber outros valores além de cores sólidas, como imagens e gradientes. A diferença entre img e o background é que a imagem faz parte do conteúdo, o background apenas o estilo.
![[img-68.png]]
```css
.galaxia{
  height: 600px;

  background-color: cadetblue;
  background-image: url(../05-images/imgs/bryan-goff-f7YQo-eYHdM-unsplash.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;

  background: turquoise url(../05-images/imgs/bryan-goff-f7YQo-eYHdM-unsplash.jpg) no-repeat center cover; 

}
```
- Usar apenas a propriedade background e um shorthand(atalho) para todas as outras propriedades acima, e é obrigatório setar todos esses valores nessa ordem
- Padrão
	Podemos usar alguns detalhes como padrão em nossos sites.
![[img-69.png]]
```css
.pattern {
  height: 100px;
  background-color: lightblue;
  background-image: url(../img/pattern.svg);
  margin: 10px 0;
}

.pattern-y {
  height: 100px;
  background-color: lightblue;
  background-image: url(../img/pattern.svg);
  background-repeat: repeat-y;
  margin: 10px 0;
}
.pattern-x {
  height: 100px;
  background-color: lightblue;
  background-image: url(../img/pattern.svg);
  background-repeat: repeat-x;
}

```
- `linear` e `radial` gradient
![[img-70.png]]
```css
.linear{
  height: 200px;
  background-image: linear-gradient(to left, cadetblue, turquoise);
  background-image: linear-gradient(45deg, cadetblue, turquoise);
  background-image: linear-gradient(45deg, cadetblue 10%, turquoise 60%, blue 99%);
  background-image: linear-gradient(45deg, rgb(0, 247, 255), rgb(55, 87, 83));
}
.radial{
  height: 200px;
  background-image: radial-gradient(circle, rgb(170, 249, 252), rgb(0, 77, 69));
}
```
# Pseudo Class
## Estados
Permite definirmos o estilo de diferentes estados do elemento html.
- :hover
	Mouse por cima.
- :focus
	Elemento em foco, usando o teclado (tab).
- :active
	Quando clicamos no elemento.
- :visited
	Para links que já foram visitados.
![[img-71.png]]
```css
.btn{
  padding: 10px 20px;
  display: inline-block;
  margin-left: 20px;
  background-color: rgba(95, 158, 160, 0.486);
  text-decoration: none;
  color: black;
  border-radius: 5px;
  text-transform: uppercase;
  font-family: Arial, Helvetica, sans-serif;

}

.hover:hover{
  background-color: aqua;
}

.focus:focus{
  background-color: blueviolet;
}

.active:active{
  background-color: blue;
  text-decoration: underline;
}

.visited:visited{
  color: red;
}

```
## Seletores
- :first-child
	Seleciona o primeiro elemento
- :last-child
	Seleciona o último elemento
- :nth-child
	4(quarto elemento), even(pares), odd(ímpares), 3n (de 3 em 3)
![[img-72.png]]
![[img-73.png]]
```html
  <div class="container">
    <p>First-Child</p>
    <ul class="fchild">
      <li>Primeiro Elemento</li>
      <li>Segundo Elemento</li>
      <li>Terceiro Elemento</li>
      <li>Quarto Elemento</li>
      <li>Quinto Elemento</li>
    </ul>
  </div>
  <div class="container">
    <p>Last-Child</p>
    <ul class="lchild">
      <li>Primeiro Elemento</li>
      <li>Segundo Elemento</li>
      <li>Terceiro Elemento</li>
      <li>Quarto Elemento</li>
      <li>Quinto Elemento</li>
    </ul>
  </div>
  <div class="container">
    <p>Nth-Child</p>
    <ul class="nchild">
      <li>Primeiro Elemento</li>
      <li>Segundo Elemento</li>
      <li>Terceiro Elemento</li>
      <li>Quarto Elemento</li>
      <li>Quinto Elemento</li>
    </ul>
  </div>
  <div class="container">
    <p>Even-Child</p>
    <ul class="echild">
      <li>Primeiro Elemento</li>
      <li>Segundo Elemento</li>
      <li>Terceiro Elemento</li>
      <li>Quarto Elemento</li>
      <li>Quinto Elemento</li>
    </ul>
  </div>
  <div class="container">
    <p>Odd-Child</p>
    <ul class="ochild">
      <li>Primeiro Elemento</li>
      <li>Segundo Elemento</li>
      <li>Terceiro Elemento</li>
      <li>Quarto Elemento</li>
      <li>Quinto Elemento</li>
    </ul>
  </div>
  <div class="container">
    <p>3n-Child</p>
    <ul class="_3child">
      <li>Primeiro Elemento</li>
      <li>Segundo Elemento</li>
      <li>Terceiro Elemento</li>
      <li>Quarto Elemento</li>
      <li>Quinto Elemento</li>
      <li>Sexto Elemento</li>
    </ul>
  </div>
```
```css
.container{
  margin: 30px;
  border-bottom: 1px solid black;
}

.container ul{
  list-style-type: none;
}

.container ul li{
  padding: 5px 10px;
  border: 1px solid black;
  margin-bottom: 5px;
}


.fchild li:first-child{
  background-color: aquamarine;
}

.lchild li:last-child{
  background-color: cadetblue;
}

.nchild li:nth-child(4){
  background-color: cornflowerblue;
}

.echild li:nth-child(even){
  background-color: cyan;
}


.ochild li:nth-child(odd){
  background-color: rgb(0, 189, 189);
}

._3child li:nth-child(3n){
  background-color: rgb(18, 98, 179);
}

```
- :not
O `:not` nega a seleção de um elemento específico.
![[img-74.png]]
```css
.not li{
  background-color: rgb(18, 98, 179);
}
.not li:not(:first-child, :last-child){
  background-color: #fff;
}/* Todos estão brancos menos o primeiro e o último que foi selecionado*/
```
### Atributos
- `[atributo]`
	Seleciona os elementos que tiverem o atributo dentro dos `[]`
- `[name="email"]`
	Seleciona apenas o elemento que tiver o atributo e o valor
- `[href^="#"]`
	Seleciona atributos que comecem `^` com o valor `#`
- `[href$=".com"]`
	Seleciona atributos que terminam `$` com o valor `.com`
![[img-87.png]]
```css
p [required]{
/* Todos os elementos required que tiverem dentro de um p  */
  background-color: cornflowerblue;
}

a[href="#contato"]{
  /* Todos os a's que tiverem #contato */
  display: inline-block;
  border: 1px solid black;
  padding: 10px;
}

[href^="#"]{
  background-color: darkgray;
}

[href$=".com"]{
  display: inline-block;
  border: 1px solid black;
  padding: 10px;
  background-color: aliceblue;
}
```
### Sinais
- `div > p`
	Apenas `p` que for filho direto de `div`
- `p + p`
	Todo `p` que vier após um elemento `p`
- `*`
	Seleciona todos os elementos do site.
![[img-88.png]]
```css
section > h2{
  color: cornflowerblue;
}

article{
  background-color: lightblue;
  padding: 10px;
}

p + p{
  margin-top: 20px;
}
```
## ::before e ::after
Os pseudo elements ::before e ::after criam elementos HTML com base no seletor.
- content
	Definir um conteúdo para o elemento é essencial para ele existir, mesmo que o conteúdo esteja vazio.
- uso
	São utilizados para decorarmos o conteúdo, com eles evitamos o uso de elementos desnecessários no HTML.
![[img-75.png]]
```css
h1{
  margin: 20px;
  position: relative;
}h1::after{
  content: '';
  display: inline-block;
  width: 40px;
  height: 5px;
  background-color: aqua;
  position: absolute;
  bottom: 0;
  left: 0;
}


ul{
  list-style-type: none;
  margin: 20px;
}

li{
display: flex;
align-items: center;
gap: 10px;
}li::before{
  content: '';
  display: inline-block;
  width: 8px;
  height: 8px;
  border-radius: 50%;
  background-color: cadetblue;
}
```
# Responsivo
Um layout que se adapta a diferentes tipos/tamanhos de tela e a preferências do usuário.
- Tamanhos 
	Unidades relativas com %, vw e fr são mais utilizadas.
- Media Queries
	Código será ativado de acordo com o tamanho da tela. Alterar o layout, esconder itens e adicionar funcionalidades.
- Flexbox e Grid
	Manipulamos o flexbox e o grid para adaptar o conteúdo.
- Tipo de tela
	Temos que levar em consideração a operação do site apenas com o dedo
No Site stripe temos três quebras de layouts, onde em cada etapa vai desaparecendo algo que em uma tela pequeno poderia ficar escondida ou até mesmo desaparecer
- stripe em tela cheia
![[img-76.png]]
- stripe em telas médias
![[img-77.png]]
- stripe em telas pequenas
![[img-78.png]]
# Media Queries
## @media
A `@media` gera um bloco de código que só será ativado caso condição entre parênteses seja verdadeira.
- `@media (max-width: 500px)`
	abaixo de 500px
- `@media (min-width: 600px)`
	Acima de 600px
- `@media (max-width: 500px) and @media (max-width: 500px)`
	Entre 800px e 900px
![[vid-01.mp4]]
```css
.container{
  width: 100%;
  max-width: 1000px;
  height: 800px;
  display: grid;
  place-items: center;
  background-color: cadetblue;
}

img{
  max-width: 50%;
  display: block;

}

@media (max-width: 1000px) {
/* De 1000 px para baixo esse código será executado */
  .container{
    background-color: brown;
  }
}

@media (min-width: 900px) {
/* De 900px para cima código esse código será executado */
  /* .container{
    background-color: brown;
  } */
}

/* quando for criar o media e for usar tanto o min quanto o max primeiro teremos que usar o min, e depois o max */

@media (min-width: 600px) and (max-width: 800px) {
  /* Com o min vindo primeiro (e com um valor menor) e o max vindo depois (e com um valor maior) qualquer código que ofr executado aqui sera entre o menor valor (de min) e o maior valor (de max) e como se eles estivesse assim:
600px--> será executado <--800px */
  /* .container{
    background-color: brown;
  } */

}

@media (max-width: 600px) and (min-width: 800px) {
  /* nem com um valor de max menor (ou trocado de posição) o medioa e executado*/
  /* .container{
    background-color: brown;
  } */

}
```
# Grid Responsivo
O repeat com auto-fit irá gerar o total de colunas que forem necessárias para preencher a área.
![[img-79.png]]
```css
div{
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));

}
```
> [!info] Observe
Autofit está falando para criar o colunas de 300px, se o espaço que temos no navegador for menor que 300px ele não cria.
Utilizando somente o autofit teremos um problema, quando tivermos um espaço menor que 300px por exemplo 280px, essa coluna de 280px ficará vazia para resolver isso utilizamos o minmax. 
Com o minmax podemos falar tenha no minímo 300px e no máximo 1fr
# Object Fit
Preenche o elemento pai com a imagem, sem distorcer a mesma.
- object-fit
	Funciona como o background-size. Contém valores como cover, contain, fill.
- object-position
	Posicionando o objeto, indicando como ele deve ser cortado. top left, top center, etc.
![[img-80.png]]
```css
img{
  max-width: 100%;
  display: block;
}

.grid{
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1rem;
}

p{
  font-size:  1.5rem;
}

.cover img{
  height: 100%; /* O height é obrigatório */
  object-fit: cover;
  /* object-position: top center; */
}
```
# max-width
O `max-width` determina um valor máximo de largura do elemento. Não deixe os elementos livres na tela, principalmente os textos.
- `ch`
	Unidade relacionada à largura do caractere `0` da tipografia.
- Largura do texto
	Controlar o tamanho máximo da largura do texto é essencial para garantir uma boa leiturabilidade. Para corpo de texto entre 70 e 70 caracteres é o ponto ideal.
- margin: 0 auto;
	margin top e bottom 0, margin right e left automática(define valores iguais com base no espaço em branco e alinha o conteúdo ao centro.)
# Ferramentas
- Node
	Executa Javascript que manipula o sistema.
- Git e Git Bash
	Facilita o controle de versão do código
# Linha de Comando (CLI)
- Interagir com o computador através de textos
	Comando começando com $(Unix) ou >(Win)
- UNIX (Mac e Linux) vs Windows
	Bash e Zsh (Unix) | CMD e PowerShell (Windows)
[SS64 Referência de Linha de Comando](https://ss64.com/)
# NPM
- Gerenciador de pacotes
	Permite instalarmos diferentes programas e versões utilizando o comando `$ npm`
- Instalar Globalmente
	`$ npm install -g nomedopacote` |	`$ npm i -g nomedopacote`  
- Remover Globalmente
	`$ npm remove -g nomedopacote`
- Cleancss
	O pacote que vamos instalar será o cleancss, ele e feito para reduzir ao máximo o tamanho do nosso css, para instalar ele vamos ter que colocar o código: `$ npm install -g clean-css-cli`.
	Para executar usamos o código `cleancss -o arquivoqueserácriado arquivoexistente`. Como boa quando um arquivo for criado nomeamos ele como o antigo e colocamos um `.min` entre o nome do arquivo e o css: `cleancss -o style.min.css style.css`.
# Git e Github
- Git
	Sistema de controle de versão. Facilita o trabalho em equipe e o controle de mudanças entre arquivos e diretórios
- Github
	Plataforma online de hospedagem para repositórios Git. Existem outras como GitLab e Bitbucket.
Logando pelo terminal
```bash
git config --global user.name "name"
git config --global user.email "email"
```
Agora vamos adicionar todos os arquivos
```bash
git add -A // Vai adicionar todos os arquivos ao repositório.
git commit -m 'desc' // O commit serve para darmos uma descrição para os arquivos enviados
git status // Usamos status para ver se tem algum doc que sofreu alteração mas não foi para o repositório.
```
> [!info] Lembrando
> Todas as vezes que fizermos alterações no nossos arquivos temos que executar `git add -A` e `git commit`

O que temos até agora e apenas os arquivos no nosso repositório local, então vamos colocar ao vivo no Github.
1° - No Github Criamos um novo repositório.![[img-81.png]]
Para podermos ter um site hospedado na hora da criação do repositório, temos que colocar `.github.io` no final do nome
```bash
git remote add origin // Vai falar aonde temos que colocar nosso arquivos.
git branch -M main // essa linha só é necessaria caso sua branch estaja em master
git push -u origin main // Vai mandar seus arquivos para o github
```
# Formulário
## form
- form 
	A tag form é utilizada para envolver os campos de um formulário.
- action=""
	O atributo action indica o arquivo/url que será ativado ao enviarmos o formulário.
- method="`post` / `get`"
	POST(envio de informações) e GET(busca de informações).
### Input
dentro de form vamos colocar alguns tipos de tags a primeira e a input.
Teremos inputs de vários tipos como esse abaixo que é de texto.
- type
	Existem vários tipos de type para inputs onde os mais comuns são:
	1. `text` – campo de texto simples
	2. `password` – campo para senha (oculta os caracteres)
	3. `email` – valida e-mail
	4. `number` – aceita apenas números
	5. `tel` – usado para números de telefone
	6. `url` – valida URLs
	7. `search` – campo de busca (com estilo de busca)
	8. `checkbox` – caixa de seleção
	9. `radio` – botão de opção
	10. `file` – para upload de arquivos
	11. `date` – seletor de data
	12. `time` – seletor de hora
	13. `datetime-local` – data e hora local
	14. `range` – controle deslizante (slider)
	15. `color` – seletor de cor
- id
	Usado para relacionar o input e o label, com isso se clicarmos em label ele aciona diretamente o input.
- name
	Manda informações através da URL para o php. Com o envio no php teremos acesso ao `nome` e ao valor de nome `Bruce Moura`, onde `nome` será uma variável e `Bruce Moura` será o valor da variável sem o atributo `name` não podemos passar esses valores para o php. 
### Label
junto com o input temos que colocar outra tag chamada label, usamos ela para dar uma etiqueta/rotulo para os nossos inputs.
### Button 
Além de label e input temos que ter um jeito de enviar as informações do formulário, fazemos isso com o button
- type
	Em button também existem alguns types:
	1. `submit` – botão de envio
	2. `reset` – botão para limpar o formulário
	3. `button` – botão genérico
![[img-82.png]]
```html
  <form action="" >

    <label for="nome">Nome</label>
    <input type="text" id="nome" name="nome">

    <label for="senha">Senha</label>
    <input type="password" id="senha">

    <label for="email">Email</label>
    <input type="email" id="email">

    
    <label for="idade">Idade</label>
    <input type="number" id="idade">

    
    <label for="data">data</label>
    <input type="date" id="data">
    <button type="">Enviar</button>

  </form>
```
### Atributos
- placeholder=''
	Texto quando o formulário não está preenchido. (dica de preenchimento)
- required
	Define o input como obrigatório
- disable
	Desabilita o input
- minlength e maxlength
	Mínimo e máximo de caracteres.
- value
	Valor inicial do formulário.
![[img-83.png]]
```html
  <form action="" >

    <label for="nome">Nome</label>
    <input type="text" id="nome" name="nome">

    <label for="CPF">CPF</label>
    <input type="text" id="CPF" placeholder="000.000.000-00">

    <label for="senha">Senha</label>
    <input type="password" id="senha" required>

    <label for="email">Email</label>
    <input type="email" id="email" disabled>

    
    <label for="idade">Idade</label>
    <input type="number" id="idade" value="0" >

    
    <label for="data">data</label>
    <input type="date" id="data">
    <button type="">Enviar</button>

  </form>
```
### checkbox e radio
checkbox e radio são dois tipos de formulário onde um (checkbox) e um quadrado que pode ser marcado e o outro (radio) é uma bolinha que pode ser selecionada, para o radio se o atributo `name` for igual para dois elementos, so 1 poderá ser selecionado.
![[img-84.png]]
```html
<div class="checkbox">
  <input type="checkbox" name="checkbox" id="checkbox">
  <label for="checkbox">Aceito os Temos e Condições da empresa</label>
</div>

<div class="checkbox">
  <input type="checkbox" name="checkbox" id="anuncio">
  <label for="anuncio">Desejo reber anúncios</label>
</div>


<p>Entregra</p>
<div class="radio">
  <input type="radio" name="retirada" id="retirada">
  <label for="retirada">Retirar no local</label>
</div>

<div class="radio">
  <input type="radio" name="retirada" id="em-casa">
  <label for="em-casa">Entrega em casa</label>
</div>


<p>Encomenda</p>
<div class="radio">
  <input type="radio" name="retirada1" id="ft1">
  <label for="ft1">Retirar no local</label>
</div>

<div class="radio">
  <input type="radio" name="retirada1" id="ft2">
  <label for="ft2">Entrega em casa</label>
</div>
```
### Select
- select
	Campo de seleção com diferentes opções (option).
- option
	Opções do campo de seleção.
![[img-85.png]]
```css
<label for="parcelas">Parcelas</label>
    <select name="parcelas" id="parcelas">
      <option value="1x">1x de R$1200</option>
      <option value="3x">3x de R$400</option>
      <option value="6x">6x de R$200</option>
      <option value="12x">12x de R$100</option>
    </select>
```
### Textarea
- textarea
	Campo para textos/ Uma caixa de mensagens
![[img-86.png]]
```html
<label for="mensagem">Mensagem</label>
<textarea name="mensagem" id="mensagem" cols="40" rows="20"></textarea>

```
## Informação pela URL
Uma coisa muito importante que vamos fazer aqui e mandar informações pela url.
- No Input radio vamos escrever `name='tipo'` (esse `tipo` pode ser qualquer outro texto), e vamos pegar o valor dele e colocar `value='seguro'`. 
- No link href vamos colocar `?tipo=seguro&produto=prata` `<a href="teste.html?tipo=seguro&produto=prata">botao</a>`
`?tipo=seguro&produto=prata` isso vai fazer o seguinte, ele vai mandar as informações tipo=seguro e produto=prata para a url, na url vamos poder pegar essas informações para que quando clicarmos no botão de compra ele ir direto para o produto que foi selecionado. 
# Propriedades customizadas
Também conhecidas como variáveis css (custom properties), permite definirmos valores no CSS que podem ser reutilizadas no nosso código.
A propriedade é herdada pelos elementos filhos. É comum definirmos as mesmas nos elementos `:root` ou `html`, assim teremos acesso à propriedade em todos os elementos do site.
- `--roxo: #caf`
	Define uma propriedade customizada.
- `var(--roxo)`
	A função var utiliza uma propriedade customizada.
![[img-89.png]]
```html
<style>
  :root{
    --cor-bg-body: #7c7c7c;
    --cor-tit-prin: #caf;
    --cor-txt: rgb(29, 0, 71);
    --font-text: arial;
  }
  body{
    margin: 220px;
    font-family: var(--font-text);
    background-color: var(--cor-bg-body);
  }
  h1{
    color: var(--cor-tit-prin);
  }
  p{
    width: 400px;
    color: var(--cor-txt);
  }
</style>
<body>
  <h1>Nossos Produtos</h1>
  <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Earum neque dolore magnam atque sunt? Dolorem earum dolores, cumque tempora facilis quam quaerat inventore laboriosam voluptatum rerum sint laborum perferendis est!</p>
</body>
```
## prefers-color-scheme
A `@media prefers-color-scheme` irá executar o código css conforme a preferência de tema do usuário. Funciona da mesa forma que o `@media querie` com o max-width, porém agora em relação ao modo escuro(dark) ou claro(light).
![[img-90.png]]
```css
html{
  background-color: var(--fundo);
}
html h1{
  color: var(--titulo);
}

html p{
  color: var(--texto);
}

@media (prefers-color-scheme: dark){
  html{
    --fundo: #222;
    --titulo: #eee;
    --texto: #bbb;
  }
}

@media (prefers-color-scheme: light){
  html{
    --fundo: #fff;
    --titulo: #111;
    --texto: #444;
  }
}
```
# CSS Utilitário
Uso de classes com propriedades pré definidas, geralmente utilizadas em bibliotecas de CSS como Bootstrap e Tailwind.
![[img-91.png]]
```html
  <h1 class="titulo-primario">
    <!-- Sem class utilitária -->
    Nossos Produtos
  </h1>
  <h1 class="texto-grande cor-texto alinhamento-texto caixa-texto">
    <!-- Class utilitária -->
    Nossos Produtos
  </h1>
```
```css
/* CSS */
.titulo-primario{
  font-size: 40px;
  line-height: 50px;
  color: #a8f;
  background-color: #111;
  padding: 10px;
  border-radius: 5px;
  max-width: 300px;
  margin: 20px auto;
  text-align: center;
}

/* CSS utilitário */
.texto-grande{
  font-size: 40px;
  line-height: 50px;
}

.cor-texto{
  color: #a8f;
  background-color: #111;
}

.caixa-texto{
  padding: 10px;
  border-radius: 5px;
  max-width: 300px;
}

.alinhamento-texto{
  margin: 20px auto;
  text-align: center;
}
```










































































































































































































































































































































































































