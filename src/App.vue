<script setup lang="ts">
import * as Scry from "scryfall-sdk";

// ...in some function somewhere...
const chalice = await Scry.Cards.byName("Chalice of the Void");
console.log(chalice.name, chalice.set); // "Chalice of the Void", "a25"

const prints = await chalice.getPrints();
console.log(prints.length); // 7
</script>

<template></template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
