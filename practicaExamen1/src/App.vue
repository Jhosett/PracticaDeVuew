<script setup>
import { pushScopeId, ref } from 'vue';


let indice

let Fecha
let Peso
let TallaCintura
let TallaCadera

let array = ref([
  
])


function mandarDatos() {
  let objeto = {
    fecha: Fecha,
    peso: Peso,
    tallaCin: TallaCintura,
    tallaCad: TallaCadera
  }
  
  array.value.push(objeto)
}

</script>

<template>
  <div class="w-[30%] bg-blue-600 m-[3%] p-2">
    <ul class="space-y-2">
      <li v-for="(obj, indice) in array" :key="indice" class="text-blue-200 font-semibold">{{ array }}</li>
    </ul>
  </div>

  <div class="bg-blue-600 w-[30%] p-6 m-[3%]">
    <input v-model="Fecha" class="w-[100%] px-3 mb-3" placeholder="Fecha" type="text">
    <input v-model="Peso"  class="w-[100%] px-3 mb-3" placeholder="Peso" type="text">
    <input v-model="TallaCintura" class="w-[100%] px-3 mb-3" placeholder="Talla cintura" type="text">
    <input v-model="TallaCadera" class="w-[100%] px-3 mb-3" placeholder="Talla cadera" type="text">
    <button @click="mandarDatos()" class="bg-white p-1 ml-[85%] hover:bg-blue-950 hover:text-white hover:cursor-pointer">Añadir</button>
  </div>
</template>

