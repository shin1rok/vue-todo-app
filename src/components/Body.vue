<template>
  <div id="body">
    ぼでー
    <Todo/>
  </div>
</template>

<script>
  import Todo from './Todo.vue'

  export default {
    name: 'Body',
    components: {
      Todo
    }
  }
</script>

<style scoped>
  #body {
    margin-top: 30px;
    text-align: center;
  }
</style>
