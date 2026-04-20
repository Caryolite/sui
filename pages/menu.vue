<template>
  <div class="menu-wrapper">
    <!-- Close Button -->
    <button class="close-btn" aria-label="Close Menu">
      <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M18 6L6 18M6 6L18 18" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
      </svg>
    </button>

    <!-- Menu Items -->
    <div class="menu-items">
      <div class="menu-item" id="home">
        <span class="menu-title">歲歲今朝</span>
        <span class="menu-subtitle">Home</span>
      </div>
      <div class="menu-item" id="character">
        <span class="menu-title">歲獸代理人</span>
        <span class="menu-subtitle">Character</span>
      </div>
      <div class="menu-item" id="story">
        <span class="menu-title">邸報</span>
        <span class="menu-subtitle">Story</span>
      </div>
      <div class="menu-item" id="note">
        <span class="menu-title">後記</span>
        <span class="menu-subtitle">Note</span>
      </div>
    </div>
  </div>
</template>

<script setup>
</script>

<style scoped>
.menu-wrapper {
  background-color: #1B1A17;
  width: 100%;
  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  color: white;
  font-family: 'Noto Sans TC', sans-serif;
}

.close-btn {
  position: absolute;
  top: 20px;
  right: 20px;
  background: none;
  border: none;
  cursor: pointer;
  width: 40px;
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.close-btn svg path {
  stroke: white;
}

.menu-items {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 40px;
}

.menu-item {
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.menu-title {
  color: #F4F4F4;
  font-family: ZhaohuaMinA;
  font-size: 24px;
  font-weight: 700;
  line-height: 22px;
  letter-spacing: -4px;
  width: 162px;
  height: 22px;
  overflow: visible;
  white-space: nowrap;
}

.menu-subtitle {
  font-size: 12px;
  color: #827E7E;
}

/* Lines connecting menu items */
#home::after {
  content: '';
  position: absolute;
  width: 2px;
  height: 50px;
  background: #D4A373;
  top: 100%;
  left: 50%;
  transform: translateX(-50%);
}

#character::after {
  content: '';
  position: absolute;
  width: 2px;
  height: 50px;
  background: #D4A373;
  top: 100%;
  left: 50%;
  transform: translateX(-50%);
}

#story::after {
  content: '';
  position: absolute;
  width: 2px;
  height: 50px;
  background: #D4A373;
  top: 100%;
  left: 50%;
  transform: translateX(-50%);
}

#note::after {
  content: '';
  position: absolute;
  width: 2px;
  height: 0;
  background: transparent;
  top: 100%;
  left: 50%;
  transform: translateX(-50%);
}


</style>