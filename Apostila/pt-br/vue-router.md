# Webschool.io - Curso Vue.js 2 - Apostila


## `vue-router`

O `vue-router` é um add-on oficial do Vue.js responsável por criar e manter as rotas das nossas aplicações. Ele foi desenvolvido pela própria equipe de desenvolvimento do Vue.js e ele se integra nas nossas aplicações de forma nativa.

Nas versões mais atuais do **vue-cli** já é possível instalar o `vue-router` na instalação do template padrão. Caso não seja instalado já via **vue-cli** o comando para instalação é `npm install --save vue-router`.

Agora, vamos configurar o `vue-router` em nossa aplicação.

No arquivo `main.js` devemos:

1. Importar o `vue-router`;  
2. Dizer ao Vue para utilizar o `vue-router`;  
3. Criar as rotas;  
4. Chamar um `new VueRouter`;  
5. Especificar na nossa instância Vue que iremos renderizar com as rotas.

Os passos acima, estão no código abaixo, descritos com comentários o que é cada passo.

```js  
import Vue from 'vue'

// 1. Importar o `vue-router`
import VueRouter from 'vue-router'

import VueMaterial from 'vue-material'
import 'vue-material/dist/vue-material.css'

import App from './App'
import Categories from './components/categories.vue'
import Products from './components/products.vue'

Vue.use(VueMaterial)

// 2. Dizer ao Vue para utilizar o `vue-router`
Vue.use(VueRouter)

// 3. Criar as rotas
const routes = [
  { path: '/products', component: Products },
  { path: '/categories', component: Categories }
]

// 4. Chamar um `new VueRouter`
const router = new VueRouter({
  routes
})

Vue.material.registerTheme('default', {
  primary: 'blue',
  accent: 'red',
  warn: 'red'
})

/* eslint-disable no-new */
new Vue({
  // 5. Especificar na nossa instância Vue que iremos renderizar com as rotas
  router,
  render: (h) => h(App)
}).$mount('#app')
```

Assim é possível criarmos as rotas necessárias para a nossa aplicação.

Maiores informações quanto ao `vue-router`, basta vermos a sua documentação oficial, [nesse link](http://router.vuejs.org/en/).
