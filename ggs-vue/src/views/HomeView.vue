<script setup lang="ts"></script>

<template>
  
  <div id="main">
    <WebHead :need_search="true" />
    <WebSearch />

    <AdCardDeck />
    <QuickBar/>
    <RankSort/>
  </div>

</template>

<style scoped>
  #main {
    width: 100%; height: 100vh;
  }
</style>

<script lang="ts">
import WebHead from '../components/WebHead.vue'
import WebSearch from '../components/WebSearch.vue'
import Category from '../components/Category.vue'
import AdCardDeck from '../components/AdCardDeck.vue'
import QuickBar from '../components/QuickBar.vue'
import RankSort from '../components/RankSort.vue'

export default {
  components: {
    WebHead,
    WebSearch,
    Category,
    AdCardDeck,
    QuickBar,
    RankSort,
  },
  props: {
    need_search: {
      type: Boolean,
      default: false,
    },
    need_icon: {
      type: Boolean,
      default: false,
    },
  },
}
</script>
