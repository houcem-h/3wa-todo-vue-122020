<template>
  <div class="dali">
    <img alt="Vue logo" src="./assets/logo.png">
    <Todos></Todos>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Todos from './components/Todos.vue'

export default {
  name: 'App',
  components: {
    HelloWorld, Todos
  }
}
</script>

<style>
.dali {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
