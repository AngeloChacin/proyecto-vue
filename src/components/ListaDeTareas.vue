<template>
    <div>
        <h2>Lista de Tareas</h2>
        <p>
            <!-- https://es.vuejs.org/v2/guide/events -->
            <input type="text" v-model="nuevaTarea" v-on:keyup.enter="taskAdd"  placeholder="Enter para confirmar">
            <!-- <input type="text" v-model="nuevaTarea" @keyup.enter="taskAdd"  placeholder="Enter para confirmar"> -->
            <!-- <input type="text" v-model="nuevaTarea" @keyup.page-down="taskAdd"  placeholder="Enter para confirmar"> -->
        </p>
        <ul>
            <li v-for="(tarea, index) in tareas" :key="index">
                {{ tarea }}
            </li>
        </ul>
    </div>

</template>

<script setup>
import { ref } from 'vue';
const tareas = ref([]); //Arreglo
const nuevaTarea = ref(''); //Variable reactiva vinculada al input mediante v-model

const taskAdd = () => {
    console.log(nuevaTarea.value);
    tareas.value.push(nuevaTarea.value); //añadir a la coleccion
    nuevaTarea.value = ''; //limpiar variable reactiva
}
</script>

<style>
li {
  color: red;  
}

</style>