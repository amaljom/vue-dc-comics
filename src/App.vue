<template>
  <div id="App"> 
    <header/>
  </div>
</template>

<script>
import header from './components/header.vue'
import main from './components/main.vue'
import footer from './components/footer.vue'

export default {
  name: 'App',
  components: {
    main,
    header,
    footer
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
