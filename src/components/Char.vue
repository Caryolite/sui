<script setup>
import { ref } from 'vue'

// 模擬資料來源
const cards = ref([
  { id: 1, title: '森林之美', content: '探索大自然的奧秘。', color: '#e1f5fe' },
  { id: 2, title: '都市縮影', content: '快節奏的生活步調。', color: '#fff9c4' },
  { id: 3, title: '深海世界', content: '潛入未知的蔚藍海域。', color: '#c8e6c9' },
  { id: 4, title: '沙漠之旅', content: '體驗熱帶的激情。', color: '#ffcc80' },
  { id: 5, title: '雪山之巅', content: '挑戰極限的高度。', color: '#b3e5fc' }
])
</script>

<template>
  <div class="card-container">
    <!-- 使用 v-for 循環渲染 -->
    <div 
      v-for="item in cards" 
      :key="item.id" 
      class="card"
      :style="{ backgroundColor: item.color }"
    >
      <h3>{{ item.title }}</h3>
      <p>{{ item.content }}</p>
      <button @click="alert('點擊了 ' + item.title)">了解更多</button>
    </div>
  </div>
</template>

<style scoped>
.card-container {
  display: flex;
  gap: 16px;
  flex-wrap: wrap;
}

.card {
  border: 1px solid #ddd;
  border-radius: 8px;
  padding: 20px;
  width: 200px;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}
</style>