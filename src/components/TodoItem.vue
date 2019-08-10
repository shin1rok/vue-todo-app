<template>
  <div id="todo-item">
    <li>
      {{todo.title}}
      <button @click="$emit('remove', todo.id)">
        X
      </button>
    </li>
  </div>
</template>

<script>

  export default {
    name: 'TodoItem',
    props: {
      todo: {
        type: Object,
        required: true
      }
    }
  }
</script>

<style scoped>
  #todo-item {
  }
</style>
