<template>
  <form @submit.prevent="addNewTodo">
      <div class="input-group mb-3">
        <input v-model="title" type="text" name="title" id="title" class="form-control" placeholder="Add Todo ...">
        <div class="input-group-append">
            <button :disabled="title === ''" type="submit" class="btn btn-outline-secondary">Add !</button>
        </div>
      </div>
  </form>
</template>

<script>
export default {
    name: 'NewTodo',
    data() {
        return {
            title: ''
        }
    },
    methods: {
        addNewTodo: function() {
            this.$emit('addTodo', this.title);
            this.title = '';
        }
    }
}
</script>

<style>

</style>