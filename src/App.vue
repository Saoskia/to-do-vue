<template>
  <div id="app">
    <div class="smaller-container">
      <div class="flex-row">
        <div class="flex-small one-fourth"></div>
        <div class="flex-small half">
          <h1>To Do List</h1>
          <NewForm />
          <ToDoList />
        </div>
        <div class="flex-small one-fourth"></div>
      </div>
    </div>
  </div>
</template>

<script>
import NewForm from './components/NewForm.vue'
import ToDoList from './components/ToDoList.vue'

export default {
  name: 'App',
  components: {
    NewForm,
    ToDoList
  }
}
</script>

<style>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
