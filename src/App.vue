<script setup lang="ts">
import NavMenu from "./components/NavMenu.vue";
</script>

<template>
  <NavMenu />
</template>

<style>

@import url('https://fonts.cdnfonts.com/css/nexa');
@import url('https://fonts.cdnfonts.com/css/dm-sans');

:root {
  --primary-color: rgba(11,00,31, 1);
  --overlay-color: rgba(11,00,31, 0.90);
  --menu-speed: 0.75s;
  font-size: 62.5%;
}

body {
  background: #fff;
  font-family: 'Nexa', sans-serif;
  color: #110031;
  text-align: center;
  font-size: 2.8rem;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
  margin: 0;
}

h1 {
  font-family: 'Nexa', "Tibetan Machine Uni";
  font-size: 2.9rem;
}

h2 {
  font-size: 2.4rem;
  font-family: "DM Sans";
}

a {
  font-size: 2.1rem;
}
</style>
