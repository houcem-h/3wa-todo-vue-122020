<template>
  <div>
    <Navbar></Navbar>
    <router-view class="container py-3"/>
  </div>
</template>
<script>
import Navbar from './components/Navbar'
export default {
  components: {
    Navbar
  }
}
</script>

<style>

</style>
