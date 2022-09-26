<template>
  <div v-html="favBands" />
  <h1 :id="idBinding">{{ band1 }}</h1>
  <h1>{{ band2 }}</h1>
  <h1>{{ band3 }}</h1>
  <h1 :class="classBinding">{{ band4 }}</h1>
  <button :disabled="isDisabled">{{ band5 }}</button>
  <!-- Se puede quitar el paréntesis en el @click-->
  <button @click="helloWorld()">CLICK ME!</button>
</template>

<script setup>
import { ref } from "vue";
let band1 = ref("Extremoduro");
let band2 = ref("Doble V");
let band3 = ref("Dr. Dre");
let band4 = ref("SFDK");
let band5 = ref("Residente");

function helloWorld() {
  // `this` inside methods points to the current active instance
  console.log(`Hello World`);
  alert("Hello World");
}
</script>

<style scoped></style>
