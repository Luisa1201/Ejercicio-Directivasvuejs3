<script setup>
import {ref, computed } from 'vue'
const users = [
  {
    name: 'Jhon',
    lastame: 'Doe',
    age: 30
  },
  {
    name: 'Jane',
    lastame: 'Doe'

  }
  ]
const msg = 'asdasd'
const num = ref(0)

num.value = 2

const computado = computed(function (){
  return num.value > 0 ? num.value * 2 : 0
})
/*const mostrar = () =>{
  alert('Me están llamando')
}*/

/*const mostrar = function(){
  alert('Me están llamando')
}*/

/*const computado = computed(function (){
  if(num.value > 0){ //Si el valor es mayor a cero hace el num.value * 2 y si else retorna 0.
    num.value * 2
  } else{
    return 0
  }
})*/

/*function mostrar() {
  alert('Me están llamando') //muestra alerta

}*/

</script>

<template>
  Hola mundo {{ msg }} <br>
  Valor {{ num }} <br>
 {{ mostrar }} <br>   <!--mostrar alerta mostrar() o mensajes mostrar -->
  Valor computado {{ computado }}

  <div v-for="(user, index) in users" :key="index">
    Nombre Completo: {{ user.name }} {{ user.lastame }} <br>
    <span v-if="user.age">
      Edad: {{ user.age }}
    </span>
  </div>

  
</template>

<style scoped>

</style>
