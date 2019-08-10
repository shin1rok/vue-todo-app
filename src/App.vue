<template>
  <div id="app">
    <Header title="Todo App"/>
    <Body/>
  </div>
</template>

<script>
  import Header from './components/Header.vue'
  import Body from './components/Body.vue'

  export default {
    name: 'app',
    components: {
      Header,
      Body
    }
  }
</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;

    /*color: #2c3e50;*/
    /*margin-top: 60px;*/
  }
</style>
