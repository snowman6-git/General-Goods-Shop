<template>
  <main id="main">
    <h1 style="transform: translateY(-10vh);">주간 HOT템</h1>


    <div id="rank_case">
      <ProductPreview event="HOT세일" name="장난치기좋은 고무느낌 철망치" price="29,800"/>
      <ProductPreview event="대량입고" name="교수님의 모든것을 알고싶은 아두이노 키로거" price="119,800"/>
      <ProductPreview event="환불불가" name="아무생각없이 보기좋은 김하진 포카 3장 랜덤발송" price="3,800"/>
    </div>
  
  </main>
</template>

<script lang="ts">

import ProductPreview from './ProductPreview.vue'
export default {
  components: {
    ProductPreview,
  }
}
</script>

<style scoped>
#main {
  border-top: 0.1rem solid rgba(255, 255, 255, 0.5);
  text-align: center;
  width: 100%; height: 100%;
  /* background-color: red; */
  display: flex;
  justify-content: center;
  flex-direction: column;
}
#rank_case{
  width: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;

  gap: 3rem;
}
</style>
