<template>
  <div id="app">
  <div class="smaller-container">
      <div class="flex-row">
    <div class="flex-small one-fourth"></div>
    <div class="flex-small half">
          <h1>To Do List</h1>
          <NewForm @on-new-todo="addNewItem(newItem)" />
          <ToDoList :newItem="newItem" />
          <div class="footer text-center">
      <!-- Heart SVG from https://feathericons.com/ -->
      Made with <img src="../src/assets/heart.svg" alt="love"> during quarantine.
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
  },
  data () {
    return {
      newItem: ''
    }
  },
  methods: {
    addNewItem(item) {
      this.newItem = item;
    }
  }
}
</script>

<style>
  .footer {
  font-size: 0.9em;
  margin-top: 40px;
  }

  .footer img {
  width: 13px;
  margin-bottom: -1px;
  }
</style>
