<script setup lang="ts">
import NavMenu from "./components/NavMenu.vue";
</script>

<template>
  <NavMenu />
</template>

<style scoped>

@import url('https://fonts.cdnfonts.com/css/nexa-bold');
@import url('https://fonts.cdnfonts.com/css/dm-sans');

:root {
  font-size: 62.5%;
}

body {
  background: #fff;
  font-family: 'Nexa Bold', sans-serif;
  color: #110031;
  text-align: center;
  font-size: 2.8rem;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
}

/*
nav a:first-of-type {
border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
*/
</style>
