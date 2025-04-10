<template>
  <div id="head">
    <div id="title">
      <!-- <img v-show="need_icon" class="hicon" src="/logo.svg" alt="" /> -->
      <h1>❚청년잡화</h1>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  props: {
    need_icon: {
      type: Boolean,
      default: true,
    },
  },
}
</script>

<style scoped>
h1 {
  font-weight: 600;
  font-size: 1.5rem;
}
.hicon {
  height: 2rem;
  width: auto;
  margin-right: 0.5rem;
  border-radius: 50%;
}
#title {
  display: flex;
  align-items: center;
}
</style>
