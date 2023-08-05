<script setup lang="ts">
import Hero from "../components/Hero.vue";
import MySkills from "../components/MySkills.vue";
</script>

<template>
  <main>
    <Hero />
    <MySkills />
  </main>
</template>

<style>
  main {
    min-height: 100vh;
    min-width: 100%;
    display: flex;
    justify-content: start;
    flex-direction: column;
    flex-wrap: wrap;
    align-content: center;
    border: solid 1px red;
  }

  h1 {
    padding: 3rem 0 3rem 0;
    font-size: 8vw;
  }
</style>
