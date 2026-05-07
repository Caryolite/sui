<script setup>
import { ref } from 'vue';
import Home from './components/Home.vue';
import Menu from './components/Menu.vue';
import CharList from './components/CharList.vue';
import Char from './components/Char.vue';

// 切換menux`
const isMenuOpen = ref(false)

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}
</script>

<template>
  <div class="w-[402px] m-auto absolute">
    <!-- <Home @openMenu="toggleMenu" v-if="!isMenuOpen"/> -->
    <!-- <Menu class="absolute t-0" @closeMenu="toggleMenu" v-if="isMenuOpen" /> -->
    <CharList/>
    <!-- <Char/> -->
  </div>
</template>

<style>
:root {
  --color-white: #F4F4F4;
  --color-background: #1B1A17;
  --color-gray: #827E7E;
  --color-dark-gray: #554E4E;
  --color-orange: #F0781C;
  --color-red: #9C1F1F;
}

body {
  background: var(--color-background);
  min-height: 100vh;
  /* display: flex; */
  justify-content: center;
  width: 402px;
  margin: auto;
}

/* Header */
.site-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  width: 366px;
  height: 60px;
  backdrop-filter: blur(4px);
  z-index: 10;
  margin: 80px 20px 40px 20px;
}
.site-title {
  color: var(--color-white);
  font-family: 'ZhaohuaMinA';
  font-feature-settings: 'liga' off, 'clig' off;
  font-weight: bold;
  line-height: 22px;
  letter-spacing: -10px;
  width: 162px;
  height: 22px;
  overflow: visible;
  white-space: nowrap;
  margin: 0;
}
.site-subtitle {
  color: var(--color-white);
  font-feature-settings: 'liga' off, 'clig' off;
  font-size: 10px;
  font-weight: 300;
  line-height: 22px;
  /* margin-top: 16px; */
}
.menu-btn {
  background: none;
  border: none;
  cursor: pointer;
  padding: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 0;
}

.page-wrapper {
  width: 402px;
  min-height: 874px;
  /* background: var(--color-background); */
  position: relative;
  overflow: hidden;
}

/* Top gradient overlay */
/* .top-gradient-overlay {
  width: 402px;
  height: 177px;
  background: linear-gradient(180deg, var(--color-background) 0%, rgba(27, 26, 23, 0.00) 100%);
  filter: blur(4px);
  position: absolute;
  margin: auto;
  top: -15px;
  pointer-events: none;
  z-index: -1;
} */

</style>