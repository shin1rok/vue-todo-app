<template>
  <div id="todos">
    <!--TODO.vueに書きたい-->
    <BaseInputText
        v-model="newTodoText"
        placeholder="New todo"
        @keydown.enter="addTodo"
    />
    TODO一覧
    <ul v-if="todos.length">
      <TodoItem
          v-for="todo in todos"
          :key="todo.id"
          :todo="todo"
          @remove="removeTodo"
      />
    </ul>
    <p v-else>
      Nothing left in the list. Add a new todo in the input above.
    </p>
  </div>
</template>

<script>
  import BaseInputText from './BaseInputText.vue'
  import TodoItem from "./TodoItem";

  let nextTodoId = 1

  export default {
    name: 'Todos',
    components: {TodoItem, BaseInputText},
    data() {
      return {
        newTodoText: '',
        todos: [
          {
            id: nextTodoId++,
            title: 'Learn Vue'
          },
          {
            id: nextTodoId++,
            title: 'Learn about single-file components'
          },
          {
            id: nextTodoId++,
            title: 'Fall in love'
          }
        ]
      }
    },
    methods: {
      addTodo() {
        const trimmedText = this.newTodoText.trim()
        if (trimmedText) {
          this.todos.push({
            id: nextTodoId++,
            title: trimmedText
          })
          this.newTodoText = ''
        }
      },
      removeTodo(idToRemove) {
        this.todos = this.todos.filter(todo => {
          return todo.id !== idToRemove
        })
      }
    }
  }
</script>

<style scoped>
  #todos {
  }
</style>
