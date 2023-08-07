<script setup lang="ts">

import {RouterLink} from "vue-router";
</script>

<template>
  <section id="ready">
    <img id="handshake" src="../assets/handshake.png" alt="Ready to work"/>
    <h1>Ready To Work</h1>
    <p>
      My years of experience and passion have culminated in an impressive resume that speaks to my credibility. I would be happy to share it with you, and I look forward to being of service.
    </p>
    <RouterLink id="preview" to="/resume">Preview Resume</RouterLink>
  </section>
</template>

<style scoped>

  #ready {
    padding-bottom: 6rem;
  }

  #handshake {
    padding-top: 6rem;
    width: 40vw;
  }

  #preview {
    background: var(--primary-color);
    color: #7ED8FF;
    padding: 2rem;
    margin: 2rem;
    border-radius: 10px;
    text-decoration: none;
  }
</style>