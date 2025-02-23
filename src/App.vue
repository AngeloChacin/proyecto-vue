<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Contador from './components/Contador.vue'
import ListaDeTareas from './components/ListaDeTareas.vue'

</script>

<template>
  <header>
    <div class="wrapper">
        <Contador></Contador>
      <br>
        <ListaDeTareas></ListaDeTareas>
    </div>
  </header>
  <RouterView />
</template>

<style scoped>
</style>
