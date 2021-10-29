# Curso Boostrap Fundamentals da Pluralsight

## O que é Boostrap?
Bootstrap é uma biblioteca virtual de código aberto capaz de oferecer padrões para o desenvolvimento HTML, CSS e JavaScript, facilitando a criação de websites mais responsivos.

----------------------------------------------------
## Adicionando um Boostrap ao seu código
O mais usual e comum é adicionar o Boostrap às sua páginas usando o CDN, por ser mais prático e de carregamento mais rápido para os navegadores, para isso basta inserir na parte de `<head>` do seu HTML o seguinte código:
``` HTML
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
```

---------------------------------------------------
## Grids
Grids são uns dos recursos fundamentais para a criação de layouts em nossos websites, por padrão no CSS toda bloco de uma grid é dividido em 12 colunas. "O sistema grid Bootstrap usa vários containers, linhas e colunas para arranjar e alinhar conteúdo." 
<br>
Toda Grid começa com um Container, `<div class= "container" > </div>`, que existem dois tipos, o padrão `<div class = "container">`, que centraliza os objetos em um container soltando espaço das bordas da página, e também o container fluído `<div class = "container-fluid">`, que ocupa 100% da página, sem soltar espaço das bordas. Para cada tipo de container, também existe sua combinação com os breakpoints, como visto na imagem a seguir:

<img width="690" alt="Captura de Tela 2021-10-27 às 11 03 06" src="https://user-images.githubusercontent.com/91977484/139081496-edd4a866-1b7c-4538-8081-f31d56e91f1f.png">

#### *Breakpoint* 
Adapta para diferentes formatar do grid.
<br><br>
Tipos de Breakpoints:
![Screen Shot 2021-10-27 at 12 57 36](https://user-images.githubusercontent.com/87997848/139102899-1a79e8b8-a097-4eae-b79c-9bc6953becd7.png)

#### *Linha e Coluna* :

A cada row(linha) pode-se ter até 12 colunas, pois o 12 é um valor que possibilita  criar diversos conceitos (2, 3 , 6 colunas).

Para se usar as colunas pode serem aplicas em `<div>` 's:

```HTML
<div class="container">
    <div class="row">
         <div class="col">
                1
         </div>  
         <div class="col-6">
                1
         </div>  
         <div class="col">
                1
         </div>  
    </div>  
</div>  
```

O tamanho de um col também  é dada pelo prefix de um breakpoint  como "col-md".

![Screen Shot 2021-10-27 at 14 08 04](https://user-images.githubusercontent.com/87997848/139113370-c0373326-2875-4014-af38-a6c029c39fe8.png)

Os prefixos como "-md"/"-xx" podem ser usados para quando a tela de um tamanhao "-sm" se organizar  no gride de uma forma se não  de outra. 

```HTML
    <div class="row">
         <div class="col-md-8 col-sm-4">
                1
         </div>   
         <div class="col-md-4 col-sm-8">
                1
         </div>  
    </div>  
```

Para empurrar seu elemento quantas colunas você deseja:
```HTML
<div class="col-md-4 offset-md-6"> <!-- O numero 6 equivale à quantas colunas para a direta deslocar-->
      ...1
</div>  
```
Para organizar de outra forma usa order-n(o valor do número vai definir para onde sera movido):
```HTML
<div class="col-md-4 order-1 ">  <!--  movido para a esquerda -->
      ...1
</div>  
```
Para deixar um pequeno  espaço entre os elementos usa-se gutter(gx-n) n define o qual largo ou nenhum com 0:
```HTML
    <div class="row gx-4">
         <div class="col-md-2">
                1
         </div>   
         <div class="col-md-4">
                1
         </div>  
    </div>  
```
---------------------------------------------------
## Estilos com Bootstrap
- Como deixar uma tabela responsiva ao tamanho da tela com Bootstrap: 

Deve-se inserir toda a tabela dentro de um `<div>`e inserir a classe "table-responsive":
  
``` HTML
     <div "table-responsive">
      <table  class="table table=striped table-bordered table hover">
          <thead>
            <tr>
              <th>Ingredients</th>
              <th>Risk</th>
              <th>Cal</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>Açúcar </td>
              <td>YEs</td>
              <td>400g</td>
            </tr>
            <tr>
              <td>Mamão  </td>
              <td>No</td>
              <td>3g</td>
            </tr>
          </tbody>
      </table>
   </div>
```
Assim quando temos uma tela menor aparecerá  um barra de scroll. 

- Como deixar uma imagem responsiva ao tamanho da tela com Bootstrap:
  
  
 Só é necessário adcionar a class="image-fluid":
  
 ``` HTML
    <div class="col-lg-4 col-sm-8">
        <img src="images/bethanylogo.png" alt="Logo"  class="rounded img-fluid/>
    </div>  
  ```
Assim a imagem irá reduzir ou almentar de acordo com o tamanho da tela.


Aplicar Padding and margin:
    
  - pb-3 : Padding bottom of 3;
                                                         
  - p-3 : Padding todos os lugares em 3;
                                                             
  - me-0: margin of right of 0;
  
  - py-5: Padding vertical of 5;                                                           

Aplicar Border:
``` HTML                                                             
 <span class="border">
  ...
 </span>                                                          
```     

---------------------------------------------------
## Componentes

#### *Progress Bar*:
Componentes de progresso são feitos com dois elementos HTML, um pouco de CSS para a largura e outros atributos. 
- Nós usamos o elemento com `.progress` como um envolto para indicar o valor máximo da barra de progresso;
- Nós usamos o elemento interno com .progress-bar para indicar o progresso da barra, até então;
- A `.progress-bar` exige um CSS inline, classe utilitária ou CSS personalizado, para definir sua largura (`style = "widht : numero %"`);
- A classe `.progress-bar` também exige o uso de alguns atributos role e aria para fazê-lo acessível.
  ``` HTML
  <div class="progress">
  <div class="progress-bar" role="progressbar" aria-valuenow="0" aria-valuemin="0" aria-valuemax="100"></div>
  </div>
  <div class="progress">
    <div class="progress-bar" role="progressbar" style="width: 25%" aria-valuenow="25" aria-valuemin="0" aria-![Captura de Tela 2021-10-28 às 09 14 59](https://user-images.githubusercontent.com/91977484/139253350-32537954-9b7c-44ae-a314-126c59aa82a6.png)
  valuemax="100"></div>
  </div>
  <div class="progress">
    <div class="progress-bar" role="progressbar" style="width: 50%" aria-valuenow="50" aria-valuemin="0" aria-valuemax="100"></div>
  </div>
  <div class="progress">
    <div class="progress-bar" role="progressbar" style="width: 75%" aria-valuenow="75" aria-valuemin="0" aria-valuemax="100"></div>
  </div>
  <div class="progress">
    <div class="progress-bar" role="progressbar" style="width: 100%" aria-valuenow="100" aria-valuemin="0" aria-valuemax="100"></div>
  </div>
  ```
  
  <br> Obtem-se a saída:

![Captura de Tela 2021-10-28 às 09 27 00](https://user-images.githubusercontent.com/91977484/139255033-706d2061-406e-4a34-934c-c401aae7de3e.png)

  
#### *Nav / NavBar*:
-Nav
O componente `.nav`cé feito com flexbox e provê uma forte fundação para construir todo tipo de componente de navegação. Ela possui sobrescrição de alguns estilos para trabalhar com listas, padding em links para criar áreas de clique maiores e estilo desativado básico.

``` HTML
  <ul class="nav">
    <li class="nav-item">
      <a class="nav-link active" href="#">Ativo</a>
    </li>
    <li class="nav-item">
      <a class="nav-link" href="#">Link</a>
    </li>
    <li class="nav-item">
      <a class="nav-link" href="#">Link</a>
    </li>
    <li class="nav-item">
      <a class="nav-link disabled" href="#">Desativado</a>
    </li>
  </ul>
```
<br> Obtem-se o seguinte resultado:

![Captura de Tela 2021-10-28 às 09 58 59](https://user-images.githubusercontent.com/91977484/139260208-c553e4bc-871c-4bd8-be97-532f6cf54302.png)

- NavBar
  - Navbars precisam de um `.navbar` com `.navbar-expand{-sm|-md|-lg|-xl}` (para responsividade) e classes do esquema de cores;
  - Navbars e seus conteúdos são fluidos, por padrão;
  - Use containers alternativos para limitar suas larguras.
  - Use nossas classes utilitárias de espaçamento e flex para controlar o espaço e alinhamento, dentro das navbars;
  - Navbars são responsivos, por padrão, mas você pode modificar isso, facilmente;
  - Comportamento responsivo depende do nosso plugin JavaScript Collapse.
  - Navbars são escondidos, por padrão, quando imprimindo. Forçe-os a serem imprimidos, usando a classe `.d-print `no `.navbar;`
  - Leia sobre a classe utilitária display.
  - Garanta acessibilidade com o elemento `<nav> `ou, se estiver usando um elemento mais genérico `(como <div>)`, coloque       `role="navigation"` em cada navbar para identificá-lo como tal, em tecnologias assistivas.
 
#### *Breadcrumbs* :
  Indica a localização da página atual, dentro de uma hierarquia de navegação e, automaticamente, coloca separadores usando CSS.
  ``` HTML
  <nav aria-label="breadcrumb">
  <ol class="breadcrumb">
    <li class="breadcrumb-item active" aria-current="page">Home</li>
  </ol>
</nav>

  <nav aria-label="breadcrumb">
    <ol class="breadcrumb">
      <li class="breadcrumb-item"><a href="#">Home</a></li>
      <li class="breadcrumb-item active" aria-current="page">Biblioteca</li>
    </ol>
  </nav>

  <nav aria-label="breadcrumb">
    <ol class="breadcrumb">
      <li class="breadcrumb-item"><a href="#">Home</a></li>
      <li class="breadcrumb-item"><a href="#">Biblioteca</a></li>
      <li class="breadcrumb-item active" aria-current="page">Dados</li>
    </ol>
  </nav>
  ```
 
 #### *Cards *:
 Os cards Bootstrap proporcionam um container de conteúdo flexível e extensível com múltiplos variantes e opções.
 ``` HTML
 <div class="card" style="width: 18rem;">
  <img class="card-img-top" src=".../100px180/" alt="Imagem de capa do card">
  <div class="card-body">
    <h5 class="card-title">Título do card</h5>
    <p class="card-text">Um exemplo de texto rápido para construir o título do card e fazer preencher o conteúdo do card.</p>
    <a href="#" class="btn btn-primary">Visitar</a>
  </div>
</div>
 ``` 
<br> Obtem-se o seguinte resultado: 

![Captura de Tela 2021-10-28 às 10 51 05](https://user-images.githubusercontent.com/91977484/139269675-392fb973-c0e0-4b13-aff4-9683e1b333f5.png)

---------------------------------------------------
## Formulários com Boostrap
Exemplo forms básico:

``` HTML
<form>
  <div class="form-group">
    <label for="exampleInputEmail1">Endereço de email</label>
    <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Seu email">
    <small id="emailHelp" class="form-text text-muted">Nunca vamos compartilhar seu email, com ninguém.</small>
  </div>
  <div class="form-group">
    <label for="exampleInputPassword1">Senha</label>
    <input type="password" class="form-control" id="exampleInputPassword1" placeholder="Senha">
  </div>
  <div class="form-group form-check">
    <input type="checkbox" class="form-check-input" id="exampleCheck1">
    <label class="form-check-label" for="exampleCheck1">Clique em mim</label>
  </div>
  <button type="submit" class="btn btn-primary">Enviar</button>
</form>
```
<br> Obtem-se o seguinte resultado: 
<img width="937" alt="Captura de Tela 2021-10-29 às 09 37 32" src="https://user-images.githubusercontent.com/91977484/139435649-6eeded34-b053-450c-b5cb-464f04162e9e.png">

---------------------------------------------------
## Fazendo páginas interativas com JavaScript-enabled components.
Para adicionar o JS , biblioteca Popper e até Jquery em seu projeto via CDN, copiar as seguintes linhas de comando:
``` HTML
  <script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.3/umd/popper.min.js" integrity="sha384-ZMP7rVo3mIykV+2+9J3UJ46jBk0WLaUAdn689aCwoqbBJiSnjAK/l8WvCWPIPm49" crossorigin="anonymous"></script>
  <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/js/bootstrap.min.js" integrity="sha384-ChfqqxuZUCnJSK3+MXmPNIyE6ZbWh2IMqE241rYiqJxyMiZ6OW/JmZQ5stwEULTy" crossorigin="anonymous"></script>
``` 
