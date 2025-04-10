<script setup lang="ts"></script>

<template>
  <WebHead :need_search="true" />
  <WebSearch />

  <AdCardDeck />
</template>

<script lang="ts">
import WebHead from '../components/WebHead.vue'
import WebSearch from '../components/WebSearch.vue'
import Category from '../components/Category.vue'
import AdCardDeck from '../components/AdCardDeck.vue'

export default {
  components: {
    WebHead,
    WebSearch,
    Category,
    AdCardDeck,
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
