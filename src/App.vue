<script setup>
import { ref } from 'vue';
import Home from './components/Home.vue';
import Menu from './components/Menu.vue';

// 切換menu
const isMenuOpen = ref(false)

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}

</script>

<template>
  <div class="w-[402px] m-auto absolute">
    <!-- 當 Home 發出 'open-menu' 信號時，執行 toggleMenu -->
    <Home @openMenu="toggleMenu" v-if="!isMenuOpen"/>
    <Menu class="absolute t-0" v-if="isMenuOpen" />
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
  align-items: flex-start;
  width: 402px;
  margin: auto;
}

.page-wrapper {
  width: 402px;
  min-height: 874px;
  /* background: var(--color-background); */
  position: relative;
  overflow: hidden;
}

/* Top gradient overlay */
.top-gradient-overlay {
  width: 402px;
  height: 177px;
  background: linear-gradient(180deg, var(--color-background) 0%, rgba(27, 26, 23, 0.00) 100%);
  filter: blur(4px);
  position: absolute;
  margin: auto;
  top: -15px;
  pointer-events: none;
  z-index: -1;
}

</style>