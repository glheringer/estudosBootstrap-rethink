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
Toda Grid começa com um Container, `<div class= "container" > </div>`
Existem Vários tipos de Containers
<img width="690" alt="Captura de Tela 2021-10-27 às 11 03 06" src="https://user-images.githubusercontent.com/91977484/139081496-edd4a866-1b7c-4538-8081-f31d56e91f1f.png">
