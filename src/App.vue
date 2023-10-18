<template>
  
  <NavBar />
    <div class="container">
      <RouterView />
    </div>

</template>

<script setup>
import { RouterView } from 'vue-router'
import NavBar from './components/Layout/NavBar.vue';

</script>



<style lang="scss" scoped>

</style>
