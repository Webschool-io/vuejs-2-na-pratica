# Webschool.io - Curso Vue.js 2.x - Exercícios


## Aula 05

Fazer o menu funcionar, abrindo na esquerda conforme explicado no vídeo.

## Nome: Lucas Frutig

## Resolvido

````````````````````````````````````

<template>
  <div id="app" class="phone-viewport">
    <md-toolbar>
      <md-button class="md-icon button" @click.native="toggleLeftSidenav">
        <md-icon>menu</md-icon>
      </md-button>
      <h1 class="md-title">{{title}}</h1>
      <md-sidenav class="md-left" ref="leftSidenav">
        <md-toolbar class="md-large">
          <div class="md-toolbar-container">
            <h3 class="md-title">Sidenav content</h3>
          </div>
        </md-toolbar>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nisi cupiditate esse necessitatibus beatae nobis, deserunt ut est fugit, tempora deleniti, eligendi commodi doloribus. Nemo, assumenda possimus, impedit inventore perferendis iusto!</p>
      </md-sidenav>
    </md-toolbar>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      title: 'Ecommerce Webschool'
    }
  },
  methods: {
    toggleLeftSidenav () {
      this.$refs.leftSidenav.toggle()
    }
  }
}
</script>

<style>

</style>


````````````````````````````````````