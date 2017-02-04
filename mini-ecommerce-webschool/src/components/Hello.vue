<template>
  <div>
    <h1>Olá coleguinhas da Webshool!</h1>

    <CcIntro></CcIntro>
  </div>
</template>

<script>
import CcIntro from './Intro.vue'

export default {
  components: {
    CcIntro
  }
}
</script>

<style scoped>
h1{
  font-size: 50px;
  font-weight: bold;
  color: #f00;
}
</style>
