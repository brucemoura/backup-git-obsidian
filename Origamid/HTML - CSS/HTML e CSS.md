O curso
> [!Summary] Sumário
> - HTML e CSS para iniciantes
> 	FronEnd, HTML, Tags, Acessibilidade, CSS, Grid Layout, Flebox, Media Queries, Responsivo, VS Code e mais.
> - Pré-requisitos
> 	Totalmente do zero
> - Ferramentas
> 	Visual Studio Code

# Projetos
- Portifólio Simples:![[img-01.png]]
- Projeto Final:![[img-02.png]]
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
![[img-03.png]]
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
![[img-04.png]]
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
![[img-05.png]]
### Id
Atributos HTML que adicionam um identificador **único** na tag. Esse identificador pode ser utilizado no CSS para selecionarmos o elemento: ``#nomeid``
![[img-06.png]]
### Class
classe em HTML adicionam um classificador que seleciona **várias** tags. Esse classificador pode ser utilizado no CSS para selecionarmos o elemento: ``.nomeclass``
![[img-07.png]]
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

![[img-08.png]]
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
![[img-09.png]]
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
![[img-10.png]]
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

![[img-12.png]]
## Caixas
Uma interface web é composta de diversas caixas que organizam o conteúdo
![[img-11.png]]
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
![[img-13.png]]
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
![[img-15.png]]
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
![[img-17.png]]
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
![[img-18.png]]
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

























































































































































































































































































































































































































































































































































































































































