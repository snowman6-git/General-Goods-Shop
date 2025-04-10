<template>
  <div id="card">
    <div id="title">{{ title }}</div>
    <p id="subtitle">{{ subtitle }}</p>
  </div>
</template>

<script lang="ts">
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    subtitle: {
      type: String,
      required: true,
    },
  },
}
</script>

<style scoped>
#title {
  font-size: 1.5rem;
}
#subtitle {
  opacity: 0.8;
  font-size: 0.75rem;
}

#card {
  display: flex;
  align-items: start;
  justify-content: center;
  flex-direction: column;
  padding: 1rem;

  min-width: 50%;
  scroll-snap-align: center;
  transition: all 0.2s;
  width: 50%;
  height: 100%;
  background-color: gray;
  border-radius: 1rem;
}
</style>
