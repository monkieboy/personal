<script setup lang="ts" defer>

import {RouterLink, RouterView} from "vue-router";



function toggle() {
  let menu  = document.getElementById('toggle') as HTMLInputElement | null;
  if (menu !== null) menu.checked = !menu.checked;
}

</script>

<template>
  <header>
    <div class="menu-wrap">
      <input type="checkbox" class="toggle" id="toggle">
      <div class="hamburger">
        <div></div>
      </div>
      <div class="nav-container">
        <h2>Mark Gray</h2>
        <nav class="menu">
          <div id="menu-overlay">
            <div style="z-index: 10000">
              <ul>
                <li>
                  <RouterLink to="/" @click="toggle">Home</RouterLink>
                </li>
                <li>
                  <RouterLink to="/resume" @click="toggle">Resume</RouterLink>
                </li>
              </ul>
            </div>
          </div>
        </nav>
      </div>
    </div>
  </header>

  <RouterView />
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
}

#menu-overlay {
  position: absolute;
  top: 50px;
}

.menu > div > div a {
  font-size: 2.6rem;
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


.menu-wrap .toggle {
  position: fixed;
  top: 1.6rem;
  right: 1.6rem;
  z-index: 2;
  cursor: pointer;
  width: 60px;
  height: 60px;
  opacity: 0;
}

.menu-wrap .hamburger {
  position: fixed;
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
.menu-wrap .toggle:checked + .hamburger > div {
  transform: rotate(135deg);
}

/* Turns Lines Into X */
.menu-wrap .toggle:checked + .hamburger > div:before,
.menu-wrap .toggle:checked + .hamburger > div:after {
  top: 0;
  transform: rotate(90deg);
}

/* Rotate On Hover When Checked */
.menu-wrap .toggle:checked:hover + .hamburger > div {
  transform: rotate(225deg);
}

/* Show Menu */
.menu-wrap .toggle:checked ~ .nav-container .menu {
  visibility: visible;
}

.menu-wrap .toggle:checked ~ .nav-container .menu > div {
  transform: scale(1);
  transition-duration: 0.75s;
}

.menu-wrap .toggle:checked ~ .nav-container .menu > div > div {
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