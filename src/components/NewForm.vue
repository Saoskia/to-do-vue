<template>
    <div class="new-form">
        <input type="text" v-model="newItem">
        <button :click="addNewItem">Add to list</button>
    </div>
</template>

<script>
export default {
    name: 'NewForm'
}
</script>

<style>
    .new-form {
        margin-bottom: 20px;
    }
</style>