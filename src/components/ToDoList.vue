<template>
    <table class="to-do-list">
        <ToDo />
        <ToDo />
    </table>
</template>

<script>
import ToDo from './ToDo.vue'

export default {
    name: 'ToDoList',
    components: {
        ToDo
    },
    props: {
        item: ToDo
    }
}
</script>