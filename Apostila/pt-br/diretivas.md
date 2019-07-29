# Webschool.io - Curso Vue.js 2.x - Apostila


## Diretivas

Diretivas são atributos diferentes dos atributos do HTML. Todas as diretivas no Vue.js possuem uma nomenclatura padrão, sempre começando com **v-** seguido pelo nome da diretiva.


# v-on

Com a diretiva **v-on** nós anexamos um ouvinte de evento ao elemento em questão. O tipo desse evento é denotado conforme o seu argumento. Para visualizar os argumentos suportados pelo **v-on**, basta acessar a documentação oficial do Vue.js, [clicando aqui](https://vuejs.org/v2/api/#v-on). Sua expressão, pode ser um nome de um método ou uma instrução inline.

Conforme a própria documentação nos diz:


> Quando usado em um elemento normal, ele só escuta eventos DOM nativos. Quando usado em um componente de elemento personalizado, ele também escuta eventos personalizados emitidos nesse componente filho.


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
