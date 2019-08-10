<template>
  <div id="todo-item">
    <li>{{todo}}</li>
  </div>
</template>

<script>

  export default {
    name: 'TodoItem',
    props: {
      todo: String
    }
  }
</script>

<style scoped>
  #todo-item {
  }
</style>
