<template>
<div class="container relative">
    <header class="site-header">
        <div class="site-title-block">
        </div>
        <button class="menu-btn" aria-label="Menu" ">
        <img src="../assets/closebtn.svg" width="30">
        </button>
    </header>

    <div class="mt-[0px] pr-45">
        <h2 @click="$emit('changePage', 'home')">歲歲今朝</h2>
        <p>home</p>
        <span class="num1">1</span>
    </div>
    <div class="line1"></div>
    <div class="mt-10 pl-40">
        <h2 @click="$emit('changePage', 'charList')">歲獸代理人</h2>
        <p>Character</p>
        <span class="num2">2</span>
    </div>
    <div class="line2"></div>
    <div class="mt-10 pr-40">
        <h2>邸報</h2>
        <p>Story</p>
        <span class="num3">3</span>
    </div>
    <div class="line3"></div>
    <div class="mt-60">
        <h2>後記</h2>
        <p>note</p>
    </div>
</div>

</template>

<script setup>
defineEmits(['changePage', 'home'], ['changePage', 'charList']);

</script>

<style scoped>
h2 {
    font-family: 'ZhaohuaMinA';
    font-feature-settings: 'liga' off, 'clig' off;
    font-size: 24px;
    font-weight: bold;
    line-height: 22px;
    letter-spacing: -4px;
    text-align: center;
    cursor: pointer;
}
p {
    text-align: center;
    font-size: 10px;
    color: var(--color-gray);
}
.line1 {
    width: 70px;
    margin: auto;
    border-top: 1px solid var(--color-orange);
    transform: rotate(37deg);
}
.line2 {
    width: 70px;
    margin: auto;
    border-top: 1px solid var(--color-orange);
    transform: translateX(-15px) translateY(10px) rotate(-35deg);
}
.line3 {
    width: 200px;
    margin: auto;
    border-top: 1px solid var(--color-red);
    transform: translateX(-40px) translateY(115px) rotate(70deg);
}
span {
    position: absolute;
    transform: translateX(60px);
}
.num1 {
    color: var(--color-orange);
    transform: translateX(160px) translateY(-60px);
}
.num2 {
    color: var(--color-orange);
    transform: translateX(180px) translateY(-60px);
}
.num3 {
    color: var(--color-orange);
    transform: translateX(85px) translateY(-60px);
}

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
  font-size: 48px;
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

</style>