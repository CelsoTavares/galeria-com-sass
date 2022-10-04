# Galeria-com-sass
### Projeto galeria desenvolvido no curso com sass
### Variáveis Sass
Sass usa o símbolo **$**, seguido por um nome, para declarar variáveis:

$myFont: Helvetica, sans-serif<br>
$myColor: red<br>
$myFontSize: 18px

body <br>
  &nbsp; font-family: $myFont<br>
  &nbsp; font-size: $myFontSize<br>
  &nbsp; color: $myColor
  <hr>

### Usando Sass !global

$myColor: red;

h1<br> 
  &nbsp; $myColor: green **!global**<br>
  &nbsp; color: $myColor<br>


p<br>
  &nbsp; color: $myColor <br>
Agora a cor do texto dentro de uma **p** tag será green!
<hr>

### Regras Aninhadas Sass

### Sintaxe sass:

nav<br>
 &nbsp; ul<br>
 &nbsp; &nbsp; margin: 0<br>
 &nbsp; &nbsp;  padding: 0<br>
 &nbsp; &nbsp; list-style: none<br>
  
  &nbsp; li<br>
   &nbsp; &nbsp; display: inline-block<br>
  
  &nbsp; a <br>
    &nbsp; &nbsp; display: block <br>
    &nbsp; &nbsp; padding: 6px 12px<br>
    &nbsp; &nbsp; text-decoration: none<br>
    
### Sintaxe CSS:

nav ul {<br>
  &nbsp; margin: 0;<br>
  &nbsp; padding: 0;<br>
  &nbsp; list-style: none;<br>
}<br>

nav li {<br>
 &nbsp; display: inline-block;<br>
}<br>
nav a {<br>
 &nbsp; display: block;<br>
 &nbsp; padding: 6px 12px;<br>
 &nbsp; text-decoration: none;<br>
}<br>

<hr>
  
### Sintaxe Sass (reset.sass):

html, <br>
body, <br>
ul, <br>
ol <br>
 &nbsp; margin: 0 <br>
 &nbsp; padding: 0 <br>

<hr>

### Sass **@mixin** e **@include**

**@mixindiretiva** permite criar código CSS que deve ser reutilizado em todo o site.

**@includediretiva** é criada para permitir que você use (inclua) o mixin.

Um mixin é definido com a **@mixindiretiva**.

O exemplo a seguir cria um mixin chamado "important-text":

**@mixin** important-text   
  &nbsp; color: red <br>
  &nbsp; font-size: 25px <br>
  &nbsp; font-weight: bold <br>
  &nbsp; border: 1px solid blue <br>

### Usando um Mixin

**@includediretiva** é usada para incluir um mixin.

Adicionando o mixin com o **@include**

.danger <br>
 &nbsp; @include important-text <br>
 &nbsp; background-color: green <br>

<hr>

### Diretiva Sass **@extend**

@extenddiretiva permite compartilhar um conjunto de propriedades CSS de um seletor para outro.

@extenddiretiva é útil se você tiver elementos de estilo quase idênticos que diferem apenas em alguns pequenos detalhes.

O exemplo Sass a seguir cria primeiro um estilo básico para botões (esse estilo será usado para a maioria dos botões). Em seguida, criamos um estilo para o botão "Relatório" e um estilo para o botão "Enviar". Ambos os botões "Report" e "Submit" herdam todas as propriedades CSS da classe .button-basic, através da @extenddiretiva. Além disso, eles têm suas próprias cores definidas:

### Sintaxe SASS:

.button-basic <br> 
 &nbsp; border: none  <br> 
 &nbsp; padding: 15px 30px  <br> 
 &nbsp; text-align: center  <br> 
 &nbsp; font-size: 16px  <br> 
 &nbsp; cursor: pointer  <br> 


.button-report   
 &nbsp; @extend .button-basic  <br> 
 &nbsp; background-color: red  <br> 

.button-submit    
 &nbsp; @extend .button-basic  <br> 
 &nbsp; background-color: green  <br> 
 &nbsp; color: white  <br> 
