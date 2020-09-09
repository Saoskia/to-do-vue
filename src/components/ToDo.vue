<template>
    <tr class="to-do">
        <td>Hello</td>
        <td class="action-buttons">
            <button class="muted-button">Edit</button>
            <button class="muted-button">Delete</button>
        </td>
    </tr>
</template>

<script>
export default {
    name: 'ToDo'
}
</script>

<style scoped>
    .to-do:hover {
        background: #eee;
    }

    .action-buttons {
        text-align: right;
    }
    .action-buttons button {
        margin: 0 2px;
    }
</style>