<template>
  <div id="App"> 
    <Header/>
    <Main/>
  </div>
</template>

<script>
import Header from './components/Header'
import Main from './components/Main'
import Footer from './components/Footer'

export default {
  name: 'App',
  components: {
    Main,
    Header,
    Footer
  }
}
</script>

<style lang="scss">
*{
    margin:0;
    padding: 0;
    box-sizing: border-box;
}
header, main, Footer{
    font-family: 'Fredoka One', cursive;
    font-family: 'Montserrat', sans-serif;
    font-family: 'Mukta', sans-serif;
    font-family: 'Open Sans', sans-serif;
    font-family: 'PT Sans', sans-serif;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
