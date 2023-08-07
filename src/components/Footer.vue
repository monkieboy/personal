<script setup lang="ts">

</script>

<template>
  <section id="footer">
    <div id="socials">
      <img class="social" src="../assets/github.png" />
      <img class="social" src="../assets/twitter.png" />
      <img class="social" src="../assets/linkedin.png" />
    </div>
  </section>
</template>

<style scoped>
  #footer {
    background: var(--primary-color);
    padding: 3rem;
  }

  #socials {
    display: flex;
    justify-content: space-evenly;
    width: 100%;
  }
  .social {
    width: 35px;
  }
</style>