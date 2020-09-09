<template>
    <table class="to-do-list">
        <tr>
            <td>Take out the trash</td>
            <td>Edit Delete</td>
        </tr>
        <ToDo />
    </table>
</template>

<script>
import ToDo from './ToDo.vue'

export default {
    name: 'ToDoList',
    components: {
        ToDo
    }
}
</script>