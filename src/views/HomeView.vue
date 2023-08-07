<script setup lang="ts">
import Hero from "../components/Hero.vue";
import MySkills from "../components/MySkills.vue";
import Knowledge from "@/components/Knowledge.vue";
import Interests from "@/components/Interests.vue";
import OpenUniversity from "@/components/OpenUniversity.vue";
import ReadyToWork from "@/components/ReadyToWork.vue";
import Footer from "@/components/Footer.vue";
</script>

<template>
  <main>
    <Hero />
    <MySkills />
    <Knowledge />
    <Interests />
    <OpenUniversity />
    <ReadyToWork />
    <Footer />
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
  }

  h1 {
    padding: 3rem 0 3rem 0;
    font-size: 8vw;
  }
</style>
