<template>
  <div id="todos">
    TODO一覧
    <ul>
      <TodoItem todo="aaa"/>
      <TodoItem todo="bbb"/>
      <TodoItem todo="ccc"/>
    </ul>
  </div>
</template>

<script>
  import TodoItem from "./TodoItem";

  export default {
    name: 'Todos',
    components: {TodoItem},
  }
</script>

<style scoped>
  #todos {
  }
</style>
