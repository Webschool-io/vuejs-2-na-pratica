# Webschool.io - Curso Vue.js 2.x - Exercícios


## Aula 05

Acrescentar um **input** no *header* e fazer com que o título atualize automaticamente conforme for digitando no **input**.

## Nome: Lucas Frutig

## Aula 05 - Resolvido

'''''''''''

<template>
  <div id="app" class="phone-viewport">
    <md-toolbar>
      <h1 class="md-title">{{title}}</h1>
      <md-input-container md-inline>
        <label>Inline field</label>
        <md-input v-model="title"></md-input>
      </md-input-container>
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
  }
}
</script>

<style>

</style>


''''''''''''
