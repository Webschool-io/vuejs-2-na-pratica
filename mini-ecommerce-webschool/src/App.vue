<template>
  <header class="phone-viewport">
    <md-toolbar>
      <md-button class="md-icon button" @click.native="toggleLeftSidenav">
        <md-icon>menu</md-icon>
      </md-button>

      <h1 class="md-title">{{ title }}</h1>
    </md-toolbar>

    <md-sidenav class="md-left" ref="leftSidenav">
       <md-toolbar class="md-medium">
         <div class="md-toolbar-container">
           <h2 class="md-title">Sidenav content</h2>
         </div>
       </md-toolbar>

       <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nisi cupiditate esse necessitatibus beatae nobis, deserunt ut est fugit, tempora deleniti, eligendi commodi doloribus. Nemo, assumenda possimus, impedit inventore perferendis iusto!</p>
     </md-sidenav>
  </header>
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
    toggleLeftSidenav () {}
  }
}
</script>

<style>
</style>
