# Webschool.io - Curso Vue.js 2.x - Apostila


## Propriedades

Quando criamos métodos no Vue Object nós o fazemos dentro de um objeto literal **{ }**, que é uma forma de iniciar um objeto usando apenas as chaves.

Este objeto de configuração possui propriedades pré-definidas pelo Vue.js, dentro das quais o desenvolvedor distribuirá seu próprio código. Esta forma de distribuição do código é uma das belezas do Vue, pois ajuda na organização geral dos seus scripts.


### data()

A propriedade data conterá um objeto com os dados do componente e que estarão disponíveis para serem mostrados no HTML.

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


### methods()

Ele irá conter todos os métodos que podemos utilizar para realizar algumas operação com os dados. Por exemplo, um método cadastrar. Conterá um objeto com todos os métodos também disponíveis ao HTML mas não limitados a ele.

Digo isso pois qualquer método contido neste objeto pode também executar os demais métodos do componente, bastando para isso utilizar o this (neste caso o this se refere ao próprio componente).

Vejamos um exemplo: 

```js  
methods: {
    addTask() {
        const task = clone(this.newTask);
        this.tasks.push(task);
    }
}
```

```html  
<button class="btn btn-default" type="button" v-on:click="addTask()">Add</button>
```

No exemplo acima, temos o método **addTask()** que é responsável por adionar uma nova *task* em nosso array. Então, em nosso HTML, chamamos esse método com o **v-on:click="addTask()".
