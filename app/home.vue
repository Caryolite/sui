<template>
  <head>
    <title>歲歲今朝：歲家的故事 --明日方舟歲家介紹</title>
  </head>

<!-- Header -->
    <header class="site-header">
      <div class="site-title-block">
        <h1 class="site-title">歲歲今朝</h1>
        <p class="site-subtitle">Arknights</p>
      </div>
      <button class="menu-btn" aria-label="Menu" @click="goToMenu">
        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M4 18C3.71667 18 3.47934 17.904 3.288 17.712C3.09667 17.52 3.00067 17.2827 3 17C2.99934 16.7173 3.09534 16.48 3.288 16.288C3.48067 16.096 3.718 16 4 16H20C20.2833 16 20.521 16.096 20.713 16.288C20.905 16.48 21.0007 16.7173 21 17C20.9993 17.2827 20.9033 17.5203 20.712 17.713C20.5207 17.9057 20.2833 18.0013 20 18H4ZM4 13C3.71667 13 3.47934 12.904 3.288 12.712C3.09667 12.52 3.00067 12.2827 3 12C2.99934 11.7173 3.09534 11.48 3.288 11.288C3.48067 11.096 3.718 11 4 11H20C20.2833 11 20.521 11.096 20.713 11.288C20.905 11.48 21.0007 11.7173 21 12C20.9993 12.2827 20.9033 12.5203 20.712 12.713C20.5207 12.9057 20.2833 13.0013 20 13H4ZM4 8C3.71667 8 3.47934 7.904 3.288 7.712C3.09667 7.52 3.00067 7.28267 3 7C2.99934 6.71733 3.09534 6.48 3.288 6.288C3.48067 6.096 3.718 6 4 6H20C20.2833 6 20.521 6.096 20.713 6.288C20.905 6.48 21.0007 6.71733 21 7C20.9993 7.28267 20.9033 7.52033 20.712 7.713C20.5207 7.90567 20.2833 8.00133 20 8H4Z" fill="white"/>
        </svg>
      </button>
    </header>

    <!-- image -->
    <div class="hero-image-wrapper">
      <img
        class="hero-image"
        src="/home-img.jpg"
        alt="歲歲今朝 Arknights"
      />
    </div>

    <!-- Glossary Section -->
    <section class="glossary">
      <p class="glossary-entry">
        <span class="term">大炎</span><br>
        <span class="definition">泰拉大陸上的一個國家。</span><br>
        <span class="term">歲</span><br>
        <span class="definition">泰拉大陸上的巨獸，擁有演化的全能。<br>幫助人們建立大炎，狩獵其他巨獸，最後被封印在歲陵。</span><br>
        <span class="term">巨獸代理人</span><br>
        <span class="definition">歲被封印後由意識中分化出來的碎片。</span><br>
        <span class="term">司歲台</span><br>
        <span class="definition">大炎官方處理歲兽的部門。</span><br>
        <span class="term">秉燭人</span><br>
        <span class="definition">司歲台中負責監視巨獸代理人的官員。</span>
      </p>
    </section>

    <!-- Footer -->
    <footer class="site-footer">
      <p class="footer-note">本網站為介紹與整理遊戲《明日方舟》歲家相關劇情。包含嚴重劇透。</p>
    </footer>

</template>

<script setup>
import { useRouter } from 'vue-router';

// Initialize the router
const router = useRouter();

// Ensure router is defined before calling push
const goToMenu = () => {
  if (router) {
    router.push('./pages/menu');
  } else {
    console.error('Router is not defined');
  }
};
</script>

<style scoped>
/* Header */
.site-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  width: 366px;
  height: 60px;
  position: absolute;
  left: 17px;
  top: 96px;
  backdrop-filter: blur(4px);
  z-index: 10;
}

.site-title-block {
  position: relative;
}

.site-title {
  color: var(--color-white);
  font-feature-settings: 'liga' off, 'clig' off;
  font-family: ZhaohuaMinA;
  font-size: 48px;
  font-weight: 700;
  line-height: 22px;
  letter-spacing: -10px;
  width: 162px;
  height: 22px;
  overflow: visible;
  white-space: nowrap;
}

.site-subtitle {
  color: var(--color-white);
  font-feature-settings: 'liga' off, 'clig' off;
  font-size: 10px;
  font-weight: 300;
  line-height: 22px;
  margin-top: 16px;
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

/* Hero Image */
.hero-image-wrapper {
  position: absolute;
  left: 20px;
  top: 190px;
  width: 360px;
  height: 203px;
}

.hero-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  aspect-ratio: 133 / 75;
  display: block;
}

/* Glossary Section */
.glossary {
  position: absolute;
  left: 17px;
  top: 411px;
  width: 363px;
}

.glossary-entry {
  color: var(--color-gray);
  font-feature-settings: 'liga' off, 'clig' off;
  font-size: 10px;
  font-weight: 400;
  line-height: 22px;
}

.term {
  color: var(--color-white);
  font-size: 10px;
  font-weight: 400;
  line-height: 22px;
}

.definition {
  color: var(--color-gray);
  font-size: 10px;
  font-weight: 400;
  line-height: 22px;
}

/* Footer */
.site-footer {
  position: absolute;
  left: 46px;
  top: 820px;
  width: 310px;
  height: 22px;
}

.footer-note {
  color: var(--color-gray);
  font-feature-settings: 'liga' off, 'clig' off;
  font-size: 10px;
  font-weight: 400;
  line-height: 22px;
  text-align: center;
  white-space: nowrap;
}

@font-face {
  font-family: 'Bender';
  src: url('/font/bender.woff2') format('woff2'),
       url('/font/bender.woff') format('woff');
  font-weight: 300; /* Light */
  font-style: normal;
}

/* Apply Bender font to all elements except the title */
body, .site-subtitle, .menu-btn, .hero-image-wrapper, .glossary, .site-footer {
  font-family: 'Bender', -apple-system, Roboto, Helvetica, sans-serif;
  font-weight: 300;
}
</style>