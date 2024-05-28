# HTML 5
O HTML (Hypertext Markup Language) é uma linguagem de marcação, que tem o objetivo de criar a estrutura para a página. Ela define o que é um título, o que é uma imagem, um link, um menu de navegação, etc.

### Tags 
Toda a estrutura da página é criada por meio de tags, elas funciona como uma etiqueta do conteúdo. 

**Sintaxe da tag**

```html
<tag> <!-- tag de abertura -->
  conteúdo
</tag> <!-- tag de fechamento -->
```
### Tags selfclosing
As tags selfclosing são tags que não possuem conteúdo e tem a abertura e fechamento na mesma tag, normalmente essa tag é acompanhada de um atributo (falaremos disso mais para frente).

```html
<tag /> <!-- tag de abertura e fechamento -->
```
### Tag de comentário

```html
<!-- conteúdo -->
<!-- aqui o navegador não vai interpretar como sendo código -->
```
### Tags de Título 

```html
<!-- Vão de h1 a h6, h1 o título com maior fonte e maior importância e assim por diante chegando no h6 o com a menor fonte e o menos importante -->
<h1>Titulo 1</h1>
<h2>Titulo 2</h2>
<h3>Titulo 3</h3>
<h4>Titulo 4</h4>
<h5>Titulo 5</h5>
<h6>Titulo 6</h6>
```
### Tags de Texto 

```html
<!-- Vão de h1 a h6, h1 o título com maior fonte e maior importância e assim por diante chegando no h6 o com a menor fonte e o menos importante -->
<p>Paragrafo</p>
<b>texto em negrito</b>
<i>texto em itálico</i>
```

### Tags de Lista 

```html
<!-- lista ordenada -->
<ol>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ol>
```

```html
<!-- lista não ordenada -->
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>
```
### Tag de Div

```html
<!-- Divisão, essa tag tem o intuito de fazer a divisão dos conteúdos -->
<div>
  Conteúdo 1
</div>
<div>
  Conteúdo 2
</div>
```
### Atributos
O atributo fornece informações a mais sobre a tag, sendo passados diretamente na tag, um atributo é composto por chave e valor, e tem a sintaxe.

```html
<tag chave="valor" />
```

### Tag de Img
```html
<!-- Tag para exibir imagem.
O atributo src deve ter no valor o caminho da imagem que deseja exibir -->

<img src="..." />
```

### Tag de Link

```html
<!-- A tag a href gera um link, onde o valor que deve ser passado no href é o link que deseja ir ao clicar no texto "Clique aqui" -->
<a href="..." />Clique aqui </a>
```

### Caminho absoluto e relativo
O caminho é um determinado arquivo se encontra, seja ele uma imagem, uma página html, um vídeo e/ou outros.

O caminho absoluto é o caminho baseado no caminho inteiro do seu computador. 
**Ex: c:/users/jess/desktop/imagem.png**

Só que esse tipo de caminho pode ser ruim, pois cada computador tem sua configuração de pasta.

E é aí que entra o caminho relativo, ele garante que não importa o computador sempre o arquivo sempre será achado, pois ele faz o caminho inverso, ou seja, de onde o arquivo está sendo chamado até o arquivo procurado.

Ex: Se o nosso projeto tem a seguinte estrutura de pasta:**

- projeto
  - sobre
    - index.html
  - imagens 
    - imagem.png

Digamos que quero chamar a **imagem.png** no **index.html**, então o caminho relativo ficaria assim:

```html
  <img src="../imagens/imagem.png" />
```
No nosso exemplo estamos saindo da pasta sobre e depois entrando na pasta imagens e pegando o arquivo imagem.png

```
./ => para partir de uma pasta

../ => é para sair de uma pasta
```
### Tags de Block e Inline
Tags em bloco (block) são tags que ocupam o espaço todo da tela horizontalmente.
Tags de linha (inline) só ocupam o espaço do conteúdo.

```html
<!-- tag em bloco -->
<h1>bloco</h1>

<!-- tag em linha -->
<a href="...">Clique aqui</a>
```
### Árvore HTML, alinhamento e indentação

![](https://raw.githubusercontent.com/diegoeis/tableless-static-images/master/2011/07/dom_tree.gif)

O html monta a estrutura da página e as estruturas podem estar dentro de outras estruturas. Ex:

```html
  <!-- a ul define que a tag é uma lista -->
  <ul>
    <!-- a li é o item da lista -->
     <li>Item 1</li>
  </ul>
```
Aqui a li está dentro da ul, pois um item da lista deve estar dentro da lista. E isso acontece em vários momentos, agrupamos tags para montar a estrutura da página.

```html
<div>
  <h1>Meu título</h1>
  <p>
    meu parágrafo 
    <b>texto em negrito</b>
  </p>
</div>
```
Toda nova tag criada no exemplo abaixo possui um novo espaçamento com o TAB do teclado, isso cria uma **indentação** que faz com que fique mais fácil entender qual tag é a tag "PAI" e qual tag é a tag "Filho".
Assim mantemos nosso código alinhado e organizado.


### Estrutura de uma página web
```html
<!-- tipo do documento -->
<!DOCTYPE html>
<!-- tag de abertura do documento HTML atribuído o idioma/língua pt-BR português do Brasil -->
<html lang="pt-BR">
<!-- Cabeçalho da aplicação, aqui fica as configurações da página -->
<head>
  <!-- define o conjunto de caracteres -->
  <meta charset="UTF-8">
  <!-- Titulo da página, fica na aba no navegador -->  
  <title>Document</title>
</head>
<!-- corpo da aplicação, aqui fica o conteúdo que será exibido na página -->
<body>
  <!-- aqui coloca o conteúdo de tela -->
</body>
</html>
```

### Tags semanticas
Tags semantica são tags com nomes mais semânticos, mais fáceis de entender o que aquela tag faz.

![](https://res.cloudinary.com/practicaldev/image/fetch/s--i1DxgY4q--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_800/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/oi1k8dwkj1d6zt0i6aqf.png)

## Criaremos a primeira página HTML

Crie uma pasta e dentro dela crie um arquivo index.html, abra o arquivo no "bloco de notas" ou em um "editor" de sua preferência, cole o código abaixo, modifique o conteúdo caso queira, salve e depois abra o arquivo novamente em um navegador.

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Meu primeiro site</title>
</head>
<body>
  <header>
    <nav>
      <a href="https://www.google.com/">Acessar Google</a>
    </nav>
  </header>
  <main>
    <section>
      <article>
        <h1>Meu título</h1>
        <h2>Subtitulo</h2>
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quos doloribus reiciendis velit ex nam.</p>
      </article>  
    </section>
    <section>
      <article>
        <h1>Meu título</h1>
        <h2>Subtitulo</h2>
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quos doloribus reiciendis velit ex nam.</p>
      </article>  
    </section>
  </main>
  <aside>
    <h2>Conteudo lateral</h2>
    <img src="https://placehold.co/100"/>
  </aside>  
  <footer>
    feito por Jess
  </footer>
</body>
</html>
```
Algo importante é lembrar que o HTML cria a estrutura mais é o CSS que fornecerá as característica da estrutura, ou seja, cor, tamanho, borda, posição e afins.


### Documentações

[w3school](https://www.w3schools.com/html/default.asp)

[MDN](https://developer.mozilla.org/pt-BR/docs/Web/HTML)