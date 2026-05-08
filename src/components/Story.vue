<script setup>
import { ref } from 'vue';
defineEmits(['changePage']);

const storyList = ref([
    {id: 1, title: '洪爐示歲', date: '2020', description: '根據古老的傳說，巨大的怪物隨時可能來襲！\n龍門這座孤城，如何用一場驚天爆炸度過難關？\n燃情鉅製《龍門末日守城》......不，應該叫《洪爐示歲》嗎！\n總之，敬請期待！'},
    {id: 2, title: '畫中人', date: '2021', description: '受到年的委託而來到大炎的炎熔與克洛絲，\n在荒野上偶遇了遇難的炎國人烏有。\n三人一起按照線索尋訪灰齊山，想要找到年的妹妹。\n小小的茅屋，在推門而入的剎那才發現竟別有天地。\n回過神來，已經身處一處風貌古樸的炎國小鎮。\n日月同懸，墨魉侵襲。一位神秘僧人，道破天機：\n真真假假，假假真真，你我皆是畫中人罷了。'},
    {id: 3, title: '將近酒', date: '2022', description: '長夢之人仍在古亭醉去，凜冽春風吹砌三山十七峰，雲翳後經年幻影露出真容。江湖舊事未竟，尚蜀已然擺開新的棋局。一位風塵僕僕德的龍門遠客，一隻藏於匣中的古董酒盞，一枚早已落入局中的旗子，一葉輕舟，划入山城。'},
    {id: 4, title: '登臨意', date: '2023', description: '矗立塞尚百年的城市，要送別一位此戍守百年的人。廟堂之高，江湖之遠。塵霾下陰謀悄然醞釀。風沙吹不動胡楊，眾志成城，無懼天災懸頂。論劍問道，搖億往事，烈酒尚有餘溫。縱橫棋路，恩怨情仇，盡歸塵土。邊鼓聲聲，遠送故人。'},
    {id: 5, title: '懷黍離', date: '2024', description: '指尖拂過稻穗，閉眼深吸，這道股之香，千年未變。睜眼，田間與她並肩揮灑汗水之人恍如當年。日來月往，他的神識早已扎根於這片土地。大地染疾，邪祟茲蔓，他仍力守這一地金黃。直至一縷飛線，飛入十二成五樓，欲還她自由。春風化雨，萬物重生。歸來是陌客，亦成自由身。他所求依舊不過是時和歲會'},
    {id: 6, title: '鏡中集', date: '2026', description: '邙山之下，一個不為人知的小鎮，處處透露著古怪。\n誦書朗朗，室無人跡，茶沸聞香，壺自斟酌。\n大好山河，繾綣思戀，嘆今生，個中滋味，棄之不捨。\n索求不過，長留人生。'},
    {id: 7, title: '相見歡', date: '2025', description: '一場離別的雨，打溼了禁城內外無數人的肩袖。一封寄往維多利亞的信，包裹起言語難明的思愁。一把突如其來的火，燒毀半生心血，好不乾淨。一鍋燉煮了百年的湯，使否來得及為他送上一線生機？或許那些所謂的「過去」，從來都稱不上什麼權謀算計，不過是人們面對無奈之事做出的無奈之舉......此事古難全。如有相見，當盡歡。'},
    {id: 8, title: '辭歲行', date: '2026', description: '一柄塵封的書刀，驚起天鏡閣內外的劍戰。一縷自遺忘中摘回的生機，喚醒了凝滯百年的煙雲。千載春秋，為分晦朔。廟堂爭執，只為拼湊一個解法。而那位以身鑄子的棋手，即將給出他的答案。自恃演化的夢想者啊，何不踏入棋枰？我是誰？汝是我，汝非我，爭之我？憑欄處，望乾坤重整，天地重秋。'}
]);
const storyUrl = [
  {id: 1, url: 'https://050644zf.github.io/ArknightsStoryTextReader/#/zh_CN/content?f=activities/act6d5/level_act6d5_st01'},
  {id: 2, url: 'https://050644zf.github.io/ArknightsStoryTextReader/#/zh_CN/content?f=activities/act16d5/level_act16d5_st01'},
  {id: 3, url: 'https://050644zf.github.io/ArknightsStoryTextReader/#/zh_CN/content?f=activities/act15side/level_act15side_st01'},
  {id: 4, url: 'https://050644zf.github.io/ArknightsStoryTextReader/#/zh_CN/content?f=activities/act23side/level_act23side_st01'},
  {id: 5, url: 'https://050644zf.github.io/ArknightsStoryTextReader/#/zh_CN/content?f=activities/act31side/level_act31side_st01'},
  {id: 6, url: 'https://050644zf.github.io/ArknightsStoryTextReader/#/zh_CN/content?f=activities/act19mini/level_act19mini_st01'},
  {id: 7, url: 'https://050644zf.github.io/ArknightsStoryTextReader/#/zh_CN/content?f=activities/act40side/level_act40side_st01'},
  {id: 8, url: 'https://050644zf.github.io/ArknightsStoryTextReader/#/zh_CN/content?f=activities/act49side/level_act49side_st01'},
]

</script>

<template>
  <div class="animation">
<!-- header -->
  <header class="site-header">
    <div class="site-title-block">
      <h1 class="site-title text-[36px]">邸報</h1>
      <p class="site-subtitle">Stories</p>
    </div>
    <button class="menu-btn" aria-label="Menu" @click="$emit('changePage')">
      <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M4 18C3.71667 18 3.47934 17.904 3.288 17.712C3.09667 17.52 3.00067 17.2827 3 17C2.99934 16.7173 3.09534 16.48 3.288 16.288C3.48067 16.096 3.718 16 4 16H20C20.2833 16 20.521 16.096 20.713 16.288C20.905 16.48 21.0007 16.7173 21 17C20.9993 17.2827 20.9033 17.5203 20.712 17.713C20.5207 17.9057 20.2833 18.0013 20 18H4ZM4 13C3.71667 13 3.47934 12.904 3.288 12.712C3.09667 12.52 3.00067 12.2827 3 12C2.99934 11.7173 3.09534 11.48 3.288 11.288C3.48067 11.096 3.718 11 4 11H20C20.2833 11 20.521 11.096 20.713 11.288C20.905 11.48 21.0007 11.7173 21 12C20.9993 12.2827 20.9033 12.5203 20.712 12.713C20.5207 12.9057 20.2833 13.0013 20 13H4ZM4 8C3.71667 8 3.47934 7.904 3.288 7.712C3.09667 7.52 3.00067 7.28267 3 7C2.99934 6.71733 3.09534 6.48 3.288 6.288C3.48067 6.096 3.718 6 4 6H20C20.2833 6 20.521 6.096 20.713 6.288C20.905 6.48 21.0007 6.71733 21 7C20.9993 7.28267 20.9033 7.52033 20.712 7.713C20.5207 7.90567 20.2833 8.00133 20 8H4Z" fill="white"/>
      </svg>
    </button>
  </header>


  <div class="container">
  
    <div v-for="story in storyList" :key="story.id">

      <div class="mx-[20px]"><a :href="storyUrl[story.id - 1].url" target="_blank" rel="noopener noreferrer">
        <div class="flex justify-between">
          <h2>{{ story.title }}</h2>
          <h3>{{ story.date }}</h3>
        </div>
        <p class="my-5">{{ story.description }}</p></a>
      </div>
   
    </div>

  </div>


    <!-- Footer -->
    <footer class="flex justify-center">
      <p class="footer-note">點擊跳轉ASTR明日方舟劇情文本閱讀器</p>
    </footer>
    <div class="m-[20px]"></div>
    </div>
</template>

<style scoped>
h2 {
    font-family: 'ZhaohuaMinA';
    font-size: 32px;
    font-weight: bold;
    line-height: 22px;
    letter-spacing: -8px;
    text-align: left;
    }
h3, p {
  color: var(--color-gray);
  font-size: 12px;
  font-weight: 400;
  line-height: 22px;
}
</style>
