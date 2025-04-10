<template>
  <div ref="cardContainer" id="panel">
    <div id="btn_case">
      <div class="btn" @click="prevCard">⯇</div>
      <div class="btn" @click="nextCard">⯈</div>
    </div>

    <AdCard
      title="아침잠이 많다면? 폭탄 알람시계!"
      subtitle="일어나지않으면 그대로 평생자버려라..."
    />
    <AdCard title="교수님! 수업 끝내주세요!" subtitle="그렇지않다면 서로 힘들어질겁니다 흐흐" />
    <AdCard title="아니~ 안취했다니까~" subtitle="숙취없다고 나대는 내 친구를 한방에 지집으로!" />
    <AdCard title="이걸 이 가격에?" subtitle="시즌아이템 대방출" />
    <AdCard title="저희 다른것도 잘해요~" subtitle="개발진이 만든 다른사이트보기" />
  </div>
</template>

<script lang="ts">
import AdCard from './AdCard.vue'

export default {
  components: {
    AdCard,
  },
  methods: {
    nextCard() {
      this.$refs.cardContainer.scrollLeft += this.$refs.cardContainer.offsetWidth
    },
    prevCard() {
      this.$refs.cardContainer.scrollLeft -= this.$refs.cardContainer.offsetWidth
    },
  },
}
</script>

<style scoped>
#btn_case {
  position: absolute;
  width: 100%;
  display: flex;
  justify-content: space-around;
}
.btn {
  width: 2rem;
  height: 2rem;
  font-size: 1rem;
  background-color: rgba(0, 0, 0, 0.8);
  border-radius: 50%;

  display: flex;
  align-items: center;
  justify-content: center;

  -webkit-user-select: none; /* Safari */
  -moz-user-select: none; /* Firefox */
  -ms-user-select: none; /* IE10+ */
  user-select: none; /* Standard syntax */
}

p {
  width: 100%;
  height: 90%;
  min-width: 100%;
  scroll-snap-align: start;
  transition: all 0.2s;
  background-color: blue;
}

#panel {
  width: 100%;
  height: 25rem;
  /* border: 0.1rem solid white; */
  display: flex;
  flex-direction: row;

  overflow: hidden;

  scroll-snap-type: x mandatory;
  scroll-behavior: smooth;

  align-items: center;
  justify-content: center;

  column-gap: 5rem;
  /* gap: 5rem; */
}
</style>
