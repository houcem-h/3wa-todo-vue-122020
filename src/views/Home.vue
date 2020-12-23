<template>
  <div class="container py-3">
    <NewTodo @addTodo="addNewTodo"></NewTodo>
    <Todos v-bind:todos="listTodos" @delete-item="deleteFromArray"></Todos>
  </div>
</template>

<script>
import Todos from '../components/Todos.vue'
import NewTodo from '../components/NewTodo'

export default {
  name: 'Home',
  components: {
    Todos, NewTodo
  },
  methods: {
    deleteFromArray: function(id) {
      // this.listTodos = this.listTodos.filter((todo) => todo.id != id);
      // ou bien 
      this.listTodos = this.listTodos.filter(
        function(todo) {
          return todo.id != id
        }
      );
    },
    addNewTodo: function(title) {
      const newTodoItem = {
        id: this.listTodos.length+1,
        title: title,
        completed: false
      };
      this.listTodos.push(newTodoItem);
    }
  },
  data() {
    return {
      listTodos: [
        {
          id: 1,
          title: 'Todo One',
          completed: false
        },
        {
          id: 2,
          title: 'Todo Two',
          completed: true
        },
        {
          id: 3,
          title: 'Todo Three',
          completed: true
        },
        {
          id: 4,
          title: 'Todo four',
          completed: false
        },
        {
          id: 5,
          title: 'Todo Five',
          completed: true
        }
      ]
    }
  }
}
</script>

<style>
</style>
