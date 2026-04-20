<template>
  <div class="page-wrapper">
    <NuxtRouteAnnouncer />

    <!-- <Menu /> -->
    <Home />

  </div>
      <div class="top-gradient-overlay"></div>
</template>


<script setup>
import "tailwindcss";

import Menu from '../pages/menu.vue';
import Home from './home.vue';


</script>


<style>
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@300;400&display=swap');

:root {
  --color-white: #F4F4F4;
  --color-background: #1B1A17;
  --color-gray: #827E7E;
  --color-dark-gray: #554E4E;
  --color-orange: #F0781C;
  --color-red: #9C1F1F;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background: var(--color-background);
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: flex-start;
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

.site-title {
  color: var(--color-white);
}

.site-subtitle {
  color: var(--color-white);
}

.glossary-entry {
  color: var(--color-gray);
}

.term {
  color: var(--color-white);
}

.definition {
  color: var(--color-gray);
}

.footer-note {
  color: var(--color-gray);
}
</style>