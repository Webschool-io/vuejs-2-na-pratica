# Webschool.io - Curso Vue.js 2 - Apostila


## Axios

O [Axios](https://github.com/mzabriskie/axios) é um client `HTTP`, responsável por realizar requisições `HTTP` em alguma API. Ele sabe interagir tant com `XMLHttpRequest` como com a interface `HTTP` do Node. Ou seja, o mesmo código que utilizarmos para fazermos nossas requisições `HTTP` no navegador também irá funcionar no servidor.

Podemos então, trabalhar com essa biblioteca em nossas aplicações em Vue.js ou em uma API desenvolvida em Node.js, por exemplo. Os códigos serão os mesmos, no front e no back.

Além dessas características, as requisições realizadas pelo Axios retornam sempre uma promise, já compátivel com o ES6.


### Instalação

`npm install --save axios` ou `bower install --save axios`


## Qual API iremos consumir?

Durante o nosso curso, paralelamente eu (Ednilson Amaral) desenvolvi uma API simples para consumirmos durante o curso. O repositório dessa API é [esse](https://github.com/ednilsonamaral/vuejs-ecommerce-api). Para mais informações sobre como desenvolvi a API, basta ler [esse artigo](http://ednilsonamaral.me/construindo-uma-api-com-hapijs-e-mongodb/).

Precisamos então, conhecer a API, saber quais são as *requests* disponíveis e como iremos trabalhar com ela. Para isso, iremos utilizar o Postman, para testes gerais antes de implementarmos em nosso código `.vue`.

Vamos efetuar o download do *postman collections* com as *requests**, disponível [nesse link](https://raw.githubusercontent.com/ednilsonamaral/vuejs-ecommerce-api/master/Ecommerce-Vue.js-na-Pratica-postman_collection-29062017-1446.json) e importá-las no nosso Postman.

Após termos importado, indo em **Collections**, visualizamos a pasta **Ecommerce Vue.js na Prática** com as requests possíveis. Temos **categorias (categories)** e **produtos (products)**.


- Criar arquivo de configuração do axios  
- Listar categorias  
- Listar uma única categoria  
- Listar produtos  
- Listar um único produto
