<template>
    <div>
        <h1>Contador</h1>
        <p>{{ contador }}</p>
        <button @click="incrementar">incrementar</button>
        <button @click="decrementar">decrementar</button>    
    </div>
</template>

<script setup>
import { ref } from 'vue';
const contador = ref(0);
//Funciones
const incrementar = ()=> {  
    contador.value++
}

const decrementar = ()=> {
  if (contador.value>0)      
      contador.value--;
}

</script>

<style scoped>
p {
    color: red;
}
</style>