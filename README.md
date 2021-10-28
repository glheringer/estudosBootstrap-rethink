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
## Componentes

#### *Progress Bar*
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
![Captura de Tela 2021-10-28 às 09 16 29](https://user-images.githubusercontent.com/91977484/139253574-1b6bb009-fab8-4ed0-9113-08bca5858921.png)

  
#### **
