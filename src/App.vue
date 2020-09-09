<template>
  <div id="app">
    <div class="smaller-container">
      <div class="flex-row">
        <div class="flex-small one-fourth"></div>
        <div class="flex-small half">
          <h1>To Do List</h1>
          <NewForm />
          <ToDoList />
          <div class="footer text-center">
            <!-- Heart SVG from https://feathericons.com/ -->
            Made with <img src="../src/assets/heart.svg" alt="love" width="13px"> during quarantine.
          </div>
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
  .footer {
    font-size: 0.9em;
    margin-top: 40px;
  }
</style>
