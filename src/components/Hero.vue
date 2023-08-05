<script setup lang="ts">

</script>

<template>
  <section id="me">
    <h1>
      <div>Hello,</div>
      <div>my name is Mark,</div>
      <div>and I am...</div>
    </h1>
    <div id="headshot-container">
      <div id="headshot"></div>
      <div id="astronomer" class="tag"><span class="star"></span><span>an astronomer</span></div>
      <div id="software-engineer" class="tag"><span class="star"></span><span>a software engineer</span></div>
      <div id="board-gamer" class="tag"><span class="star"></span><span>a board gamer</span></div>
      <div id="carpenter" class="tag"><span class="star"></span><span>a carpenter</span></div>
    </div>
  </section>
</template>

<style scoped>

#me {
  width: 100%;
  background: linear-gradient(to top, rgba(197,239,255, 0.3) 5%, rgba(228,247,255, 0.3) 85%, #fff);
  display: flex;
  align-items: center;
  flex-direction: column;
  flex-wrap: wrap;
  padding: 3rem 0 0 calc(100vw / 10);
}

#headshot {
  width: calc(100vw / 2);
  height: calc(100vw / 2 - 20px);
  border: solid 2px #6C4CDF;
  border-radius: 0.4077rem;
  position: relative;
  background: url("../assets/me.png") no-repeat;
  background-position-y: -10px;
  background-size: calc(100vw / 2) calc(100vw / 2);
}

.tag {
  display: flex;
  width: fit-content;
  height: 3rem;
  padding: 0 0.82rem 0 0.82rem;
  flex-direction: row;
  justify-content: center;
  flex-wrap: nowrap;
  align-items: center;
  flex-shrink: 0;
  font-family: "DM Sans";
  font-size: 1.2rem;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  white-space: nowrap;
  position: relative;
  color: white;
  border-radius: 0.2038rem;  }

.star {
  width: 1.3rem;
  height: 1.3rem;
  margin-right: 5px;
  flex-shrink: 0;
  background: url("../assets/star.png") no-repeat;
  background-size: 1.3rem 1.3rem;
}

#astronomer {
  background: #EA1179;
  box-shadow: 0rem 0.16rem 1.0rem 0rem rgba(240, 222, 54, 0.15);
  top: calc(-100vw / 2);
  right: calc(-100vw / 2 + 60px);
}

#software-engineer {
  background: #7ED8FF;
  box-shadow: 0rem 0.16rem 1.0rem 0rem rgba(240, 222, 54, 0.15);
  top: calc(-100vw / 2);
  right: calc(25vw);
}

#board-gamer {
  background: #F0DE36;
  box-shadow: 0rem 0.16rem 1.0rem 0rem rgba(240, 222, 54, 0.15);
  top: calc(-70vw / 2);
  right: calc(400vw / 2 / 10);
}

#carpenter {
  background: #AA4EF2;
  box-shadow: 0rem 0.16rem 1.0rem 0rem rgba(240, 222, 54, 0.15);
  top: calc(-65vw / 2);
  right: calc(-75vw / 2);
}

</style>