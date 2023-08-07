<script setup lang="ts">

</script>

<template>
  <section id="me">
    <div id="circles"></div>
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
    <div id="hexagon"></div>
  </section>
</template>

<style scoped>

#me {
  display: flex;
  align-items: center;
  flex-direction: column;
  flex-wrap: wrap;
  background: linear-gradient(to top, rgba(197,239,255, 0.4) 3%, rgba(228,247,255, 0.4) 75%);
  padding-bottom: 6rem;
}

#circles {
  position: absolute;
  top: 16rem;
  right: 80vw;
  width: calc(448px/3);
  height: calc(435px/3);
  background-image: url("../assets/circles.png");
  background-repeat: no-repeat;
  background-size: calc(448px/3);
}

#hexagon {
  background-image: url("../assets/hexagon.png");
  background-repeat: no-repeat;
  background-size: calc(256px/2);
  position: absolute;
  bottom: 126px;
  right: 0;
  width: calc(256px/3.5);
  height: calc(256px/2);
  z-index: -2;
  overflow: clip;
}

#headshot-container {
  padding: 3rem 0 0 calc(100vw / 10);
  border: solid 1px green;
  max-height: calc(100vw / 2);
  max-width: calc(100vw / 2);
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
  color: #fff;
}

#software-engineer {
  background: #7ED8FF;
  box-shadow: 0rem 0.16rem 1.0rem 0rem rgba(240, 222, 54, 0.15);
  top: calc(-100vw / 2);
  right: calc(25vw);
  color: var(--primary-color);
}

#board-gamer {
  background: #F0DE36;
  box-shadow: 0rem 0.16rem 1.0rem 0rem rgba(240, 222, 54, 0.15);
  top: calc(-70vw / 2);
  right: calc(400vw / 2 / 10);
  color: var(--primary-color);
}

#carpenter {
  background: #AA4EF2;
  box-shadow: 0rem 0.16rem 1.0rem 0rem rgba(240, 222, 54, 0.15);
  top: calc(-65vw / 2);
  right: calc(-75vw / 2);
  color: #fff;
}

</style>