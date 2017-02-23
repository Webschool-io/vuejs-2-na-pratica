# Webschool.io - Curso Vue.js 2.x - Apostila


## Two-way data binding

O *two-way data binding* é responsável por permitir ao usuário modificar as informações contidas nos componentes do Vue.js em tempo real.


## Propriedade data ( )

A propriedade **data ( )** conterá um objeto com os dados do componente e que estarão disponíveis para serem mostrados no HTML.

```js  
data () {
  return {
    title: 'Ecommerce Webschool'
  }
}
```

```html  
<md-toolbar>
  <h1 class="md-title">{{ title }}</h1>
</md-toolbar>
```

No exemplo acima, criamos a nossa propriedade **data ( )** e, inicialmente, está nos retornando um dado chamado **title** e esse mesmo dado está sendo exibido em nosso HTML.
