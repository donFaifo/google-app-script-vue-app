<script setup>
import { ref } from 'vue';
import Button from './Button.vue';
import Container from './Components/Container.vue';

const version = ref(1);

function alert(msg) {
  console.log(msg);
  version.value++;
}

</script>


<template>
  <div class="m-5 text-5xl font-black">App vue {{ version }}</div>
  <div class="m-5">
    <p class="mb-4">Esta es una prueba de aplicación de VUE con Parcel para Google App Script</p>
    <Button @click="alert('Pulsado')">Press me!</Button>
    <Button @click="version=0">Reset</Button>
  </div>
  <div class="m-5 grid grid-cols-2">
    <Container title="Contenedor 1">
      Esto es un componente Vue.
    </Container>
    <Container title="Contenedor 2">
      Esto es otra instancia del mismo componente Vue.
    </Container>
  </div>
  
</template>