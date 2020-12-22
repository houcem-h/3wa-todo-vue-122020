<template>
<div>
    <div class="list-group">
        <div v-for="todo in todos" v-bind:key="todo.id" class="list-group-item">
            <input type="checkbox" @change="toggleCompleted(todo)" v-bind:checked="todo.completed">
            <span :class="{'is-completed': todo.completed}">
                {{ todo.title }}
            </span>
            <button @click="$emit('delete-item', todo.id)" class="badge badge-danger badge-pill float-right">X</button>
            <!-- v-bind:checked <=> :checked -->
            <!-- v-on:click <=> @click -->
        </div>
    </div>
</div>
</template>

<script>
export default {
    name: 'Todos',
    props: {
        todos: Array
    },
    methods: {
        toggleCompleted: function(todo) {
            todo.completed = !todo.completed
        }
    }
}
</script>

<style>
.is-completed {
    text-decoration: line-through;
}
</style>