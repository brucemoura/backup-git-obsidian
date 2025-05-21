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
- h1, p
	A vírgula permite selecionarmos múltiplos elementos para a aplicação de um mesmo estilo
- p a
	Seleciona todos os `a` que tiverem dentro de `p` como e elemento pai (não precisa ser filho **Direto**).
![[img-05.png]]
## Id
Atributos HTML que adicionam um identificador **único** na tag. Esse identificador pode ser utilizado no CSS para selecionarmos o elemento: ``#nomeid``
![[img-06.png]]
## Class
classe em HTML adicionam um classificador que seleciona **várias** tags. Esse classificador pode ser utilizado no CSS para selecionarmos o elemento: ``.nomeclass``
![[img-07.png]]

 





























































































































































































































































































































































































































































































































































































































































































