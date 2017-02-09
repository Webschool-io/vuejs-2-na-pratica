# Webschool.io - Curso Vue.js 2.x - Apostila


## Instalação e Configuração do Vue Material

O Vue Material é um framework leve, construído com base nas especificações do Material Design. Ele foi desenvolvido para utilizarmos em projetos Vue.js. Com ele é possível criarmos aplicativos web ainda mais poderosos e bem desenhados, inclusivo no responsivo.  

Podemos criar e utilizar temas dinamicamente, utilizar seus componentes, aproveitar ao máximo dos elementos UI com uma API. Seu principal objetivo é entregar inúmeros componentes reutilizáveis e diversos elementos de interface de usuário para que possamos criar aplicações com suporte para todos os navegadores web modernos através do Vue.js 2.


# Aqui iremos apresentar sua instalação e configuração para templates desenvolvidos com `vue-cli`, especificamente o `webpack`.


### Instalação

Para instalar o Vue Material em seu projeto Vue.js é muito simples, basta executar o seguinte comando no terminal: `npm install --save vue-material`.


### Configuração

Em seu `main.js`, você precisa:  

1. Importar o `vue-material`;  
2. Importar o CSS do `vue-material`;  
3. Informar ao Vue que utilize o `vue-material`;  
4. Adicionar no `index.html` links para **Material Icons**;  
5. Registar tema **default** em `main.js`.


Após os passos acima, nosso `main.js` e `index.html` ficarão:  

```js  
import Vue from 'vue'
import VueMaterial from 'vue-material' // 1. Importar o vue-material
import 'vue-material/dist/vue-material.css' // 2. Importar o CSS do vue-material
import App from './App'

Vue.use(VueMaterial) // 3. Informar ao Vue que utilize o vue-material

// 5. Registar tema default em main.js
Vue.material.registerTheme('default', {
  primary: 'blue',
  accent: 'red',
  warn: 'red'
})

/* eslint-disable no-new */
new Vue({
  el: '#app',
  render: h => h(App)
})
```

```html  
<!DOCTYPE html>

<html>
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <title>mini-ecommerce-webschool</title>

    <link rel="stylesheet" href="//fonts.googleapis.com/css?family=Roboto:300,400,500,700,400italic">
    <link rel="stylesheet" href="//fonts.googleapis.com/icon?family=Material+Icons"> <!-- 4. Adicionar no index.html links para Material Icons -->
  </head>

  <body>
    <div id="app"></div>
    <!-- built files will be auto injected -->
  </body>
</html>
```


Feito isso, então vamos ao pequeno exemplo de um *toolbar* em nosso `App.vue`:  

```html  
<template>
  <div class="phone-viewport">
    <md-toolbar>
      <h1 class="md-title">Ecommerce Webschool</h1>
    </md-toolbar>
  </div>
</template>
```


Para visualizar os demais componentes disponíveis pelo Vue Material, basta acessar sua [documentação oficial](https://vuematerial.github.io/#/).
