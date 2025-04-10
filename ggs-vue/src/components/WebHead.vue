<template>
  <div id="panel">
    <p>청년잡화</p>
    <button>로그인</button>
  </div>
</template>

<script lang="ts">
import Logo from './Logo.vue'

export default {
  components: {
    Logo,
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

<style scoped>
#panel {
  width: 100%;
  height: 2rem;
  display: flex;
  align-items: center;
  justify-content: space-evenly;
}
</style>
