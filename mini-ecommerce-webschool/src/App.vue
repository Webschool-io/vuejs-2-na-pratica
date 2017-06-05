<template>
  <main class="phone-viewport">
    <md-toolbar>
      <md-button class="md-icon button" @click.native="toggleLeftSidenav">
        <md-icon>menu</md-icon>
      </md-button>

      <h2 class="md-title">{{ title }}</h2>
    </md-toolbar>

    <md-sidenav class="md-left" ref="leftSidenav" @open="open('Left')" @close="close('Left')">
      <md-toolbar>
        <div class="md-toolbar-container">
          <h3 class="md-title">Navegação</h3>
        </div>
      </md-toolbar>

      <md-list @click.native="closeLeftSidenav">
        <md-list-item>Perfil</md-list-item>
        <md-list-item>
          <router-link to="/categories">Categorias</router-link>
        </md-list-item>
        <md-list-item>
          <router-link to="/products">Produtos</router-link>
        </md-list-item>
        <md-list-item>Sair</md-list-item>
      </md-list>
   </md-sidenav>

   <md-row>
     <router-view></router-view>
   </md-row>
  </main>
</template>

<script>
export default {
  name: 'WebschoolComponent',

  data () {
    return {
      title: 'Ecommerce Webschool'
    }
  },

  methods: {
    toggleLeftSidenav () {
      this.$refs.leftSidenav.toggle()
    },

    closeLeftSidenav () {
      this.$refs.leftSidenav.close()
    },

    open (ref) {
      console.log('Menu aberto: ' + ref)
    },

    close (ref) {
      console.log('Menu fechado: ' + ref)
    }
  }
}
</script>

<style>
</style>
