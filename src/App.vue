<script setup>
import Home from './components/Home.vue';
import Menu from './components/Menu.vue';
</script>

<template>
  <div class="w-[402px] m-auto">
    <Menu />
    <!-- <Home /> -->
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
  display: flex;
  justify-content: center;
  align-items: flex-start;
  width: 402px;
  margin: auto;
}

.page-wrapper {
  width: 402px;
  min-height: 874px;
  background: var(--color-background);
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