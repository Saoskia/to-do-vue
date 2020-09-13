<template>
  <form @submit.prevent>
    <input type="text" v-model="newItem">
    <button @click="newToDo()">Add to list</button>
  </form>
</template>

<script>
export default {
  name: 'NewForm',
  data() {
    return {
      newItem: ''
    };
  },
  methods: {
    newToDo() {
      if (this.newItem.length > 0) {
        this.$emit("on-new-todo", this.newItem);
      }
      this.newItem = '';
    }
  }
}
</script>

<style>
  form {
    margin-bottom: 20px;
  }
</style>