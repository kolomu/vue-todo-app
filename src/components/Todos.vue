<template>
    <div>
        <div v-bind:key="todo.id" v-for="todo in todos">
            <TodoItem v-bind:todo="todo" v-on:del-todo="$emit('del-todo', todo.id)" />
        </div>
    </div>
</template>

<script>
import TodoItem from './TodoItem.vue'

export default {
    // Component name
    name: "Todos",
    components: {
        TodoItem
    },
    // accepting todos as prop in component
    props: ["todos"]
}
</script>

<style scoped>

</style>