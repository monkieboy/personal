<script setup lang="ts">

import {RouterLink, RouterView} from "vue-router";

const icons = document.querySelectorAll('.icon');
icons.forEach(icon => {
  icon.addEventListener('click', (event) => {
    icon.classList.toggle("open");
  });
});

</script>

<template>
  <header>
    <div class="menu-wrap">
      <input type="checkbox" class="toggler">
      <div class="hamburger">
        <div></div>
      </div>
      <div class="nav-container">
        <h2>Mark Gray</h2>
        <nav class="menu">
          <div>
            <div>
              <ul>
                <li>
                  <RouterLink to="/">Home</RouterLink>
                </li>
                <li>
                  <RouterLink to="/about">About</RouterLink>
                </li>
              </ul>
            </div>
          </div>
        </nav>
      </div>
    </div>
  </header>

  <RouterView/>
</template>

<style scoped>
/* https://codepen.io/bradtraversy/pen/vMGBjQ */

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

header {
  margin-bottom: 3rem;
  border: solid 1px red;
}


.menu-wrap {
  width: 100%;
  top: 0;
  left: 0;
  z-index: 1;
}

.nav-container {
  margin: auto;
  overflow: hidden;
  padding: 2.5rem 3rem;
}


.menu-wrap .toggler {
  position: absolute;
  top: 1.6rem;
  right: 1.6rem;
  z-index: 2;
  cursor: pointer;
  width: 60px;
  height: 60px;
  opacity: 0;
}

.menu-wrap .hamburger {
  position: absolute;
  top: 1.6rem;
  right: 1.6rem;
  z-index: 1;
  width: 60px;
  height: 60px;
  padding: 1rem;
  background: transparent;
  display: flex;
  align-items: center;
  justify-content: center;
}

/* Hamburger Line */
.menu-wrap .hamburger > div {
  position: relative;
  flex: none;
  width: 100%;
  height: 3px;
  background: var(--primary-color);
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.4s ease;
  border-radius: 2px;

}

/* Hamburger Lines - Top & Bottom */
.menu-wrap .hamburger > div::before,
.menu-wrap .hamburger > div::after {
  content: '';
  position: absolute;
  border-radius: 2px;
  z-index: 1;
  top: -10px;
  width: 100%;
  height: 3px;
  background: inherit;
}

/* Moves Line Down */
.menu-wrap .hamburger > div::after {
  top: 10px;
}

/* Toggler Animation */
.menu-wrap .toggler:checked + .hamburger > div {
  transform: rotate(135deg);
}

/* Turns Lines Into X */
.menu-wrap .toggler:checked + .hamburger > div:before,
.menu-wrap .toggler:checked + .hamburger > div:after {
  top: 0;
  transform: rotate(90deg);
}

/* Rotate On Hover When Checked */
.menu-wrap .toggler:checked:hover + .hamburger > div {
  transform: rotate(225deg);
}

/* Show Menu */
.menu-wrap .toggler:checked ~ .nav-container .menu {
  visibility: visible;
}

.menu-wrap .toggler:checked ~ .nav-container .menu > div {
  transform: scale(1);
  transition-duration: 0.75s;
}

.menu-wrap .toggler:checked ~ .nav-container .menu > div > div {
  opacity: 1;
  transition: opacity 0.4s ease 0.4s;
}

.menu-wrap .nav-container .menu {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  visibility: hidden;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
}

.menu-wrap .nav-container .menu > div {
  background: var(--overlay-color);
  border-radius: 50%;
  width: 200vw;
  height: 200vw;
  display: flex;
  flex: none;
  align-items: start;
  justify-content: center;
  transform: scale(0);
  transition: all 0.4s ease;
  padding-top: 9rem;
}

.menu-wrap .nav-container .menu > div > div {
  text-align: center;
  max-width: 90vw;
  max-height: 100vh;
  opacity: 0;
  transition: opacity 0.4s ease;
}

.menu-wrap .nav-container .menu > div > div > ul > li {
  list-style: none;
  color: var(--primary-color);
  font-size: 1.5rem;
  padding: 1rem;
}

.menu-wrap .nav-container .menu > div > div > ul > li > a {
  color: #fff;
  text-decoration: none;
  transition: color 0.4s ease;
}

</style>