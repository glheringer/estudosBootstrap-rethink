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

Para deixa um vazio =>  
```HTML
<div class="col-md-4 offset-md-6">
      ...1
</div>  
```
Para organizar de outra forma usa order-n(o valor do número vai definir para onde sera movido):
```HTML
<div class="col-md-4 order-1 "> // movido para a esquerda
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
