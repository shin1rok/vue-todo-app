<template>
  <div id="todo">
    入力フィールド
    <Todos/>
  </div>
</template>

<script>
  import Todos from './Todos.vue'

  export default {
    name: 'Todo',
    components: {
      Todos
    }
  }
</script>

<style scoped>
  #todo {
  }
</style>
