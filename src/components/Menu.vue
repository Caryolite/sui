<template>
<div class="container">
    <div class="mt-[180px] pr-45">
        <h2>歲歲今朝</h2>
        <p>home</p>
    </div>
    <div class="line1"></div>
    <div class="mt-10 pl-40">
        <h2>歲獸代理人</h2>
        <p>Character</p>
    </div>
    <div class="line2"></div>
    <div class="mt-10 pr-40">
        <h2>邸報</h2>
        <p>Story</p>
    </div>
    <div class="line3"></div>
    <div class="mt-60">
        <h2>後記</h2>
        <p>note</p>
    </div>
    <!-- fuck -->
</div>

</template>

<style scoped>
h2 {
    font-family: 'ZhaohuaMinA';
    font-feature-settings: 'liga' off, 'clig' off;
    font-size: 24px;
    font-weight: bold;
    line-height: 22px;
    letter-spacing: -4px;
    text-align: center;
    /* margin: 0; */
}
p {
    text-align: center;
    /* margin: 0; */
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
</style>