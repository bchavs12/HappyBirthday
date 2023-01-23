<script setup lang="ts">
import { ref } from "vue";
import JSConfetti from "js-confetti";

let name: string | object = ref(prompt("Qual seu Nome?"));

const confetti = new JSConfetti();

function showConfetti() {
  confetti.addConfetti();
}

showConfetti();
</script>

<template>
  <h1 @click="showConfetti">🎉 Happy Birthday, {{ name }}!</h1>
  <button @click="showConfetti">CONFETTI</button>
</template>

<style>
h1 {
  text-align: center;
  cursor: pointer;
  margin-top: 3em;
}
button {
  padding: 10px;
  border-radius: 5px;
  border: none;
  color: wheat;
  background: blueviolet;
  font-weight: bold;
}
</style>
