<template>
  <div class="bg-yellow-300">
    <h2 class="text-xl text">Hola, {{ name }}</h2>
    <input type="email" v-model="name" />
    <p :class="isShow">{{ email }}</p>
    <br />
    <br />
    <button @click="changeShow">Show Email</button>
  </div>
</template>

<script setup>
import { ref } from "vue";
const name = ref("Juan");
const email = ref("alex@ironhack.com");
const isShow = ref("hidden");

function changeShow() {
  if (isShow.value === "hidden") {
    isShow.value = "show";
  } else {
    isShow.value = "hidden";
  }
}
</script>

<style>
.show {
  display: block;
}

.hidden {
  display: none;
}
</style>
