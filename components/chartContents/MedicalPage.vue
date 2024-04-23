<template>
  <div class="body">
    <Subject />
    <div>
      前回のカルテ<span>2024年4月20日</span>一般内科|藤崎クリニック <span>さらに表示</span>
    </div>
    <Plan />
  </div>
</template>

<script setup lang="ts">
import Subject from '../mainMenu/Subject.vue';
import Plan from '../mainMenu/Plan.vue';
</script>

<style scoped>
.body {
  display: flex;
  flex-direction: column;
  padding: 20px;
  div {
    margin: 20px auto 20px 0;
    font-size: 0.6rem;
    color: rgb(161, 160, 160);
    span {
      margin: auto 5px; 
    }
  }
}
</style>