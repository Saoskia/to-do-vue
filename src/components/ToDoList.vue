<template>
  <table class="to-do-list">
    <NewForm
      @on-new-todo="addNewItem(newItem)"
    />
    <ToDo
      v-for="(todo, index) in todos"
      :key="index"
      :title="todo.title"
      :completed="todo.completed"
      @on-toggle="toggleToDo(todo)"
      @on-remove="removeToDo(todo)"
    />
  </table>
</template>

<script>
import NewForm from './NewForm.vue'
import ToDo from './ToDo.vue'

export default {
  name: 'ToDoList',
  components: {
    NewForm,
    ToDo
  },
  props: {
    itemTitle: String
  },
  data() {
    return {
      todos: [
        { title: 'Take out the trash', completed: true },
        { title: 'Email about party', completed: false }
      ]
    };
  },
  methods: {
    addNewItem(itemTitle) {
      this.todos.push({ title: itemTitle, completed: false })
    },
    toggleToDo(todo) {
      todo.completed = !todo.completed
    },
    removeToDo(removedTodo) {
      this.todos = this.todos.filter (todo => todo != removedTodo)
    }
  }
}
</script>