<template>
  <main>
    <p>홈</p>
    <p>핫딜</p>
    <p>타임세일</p>
    <p>희귀상품</p>
    <p>시즌</p>
    <p>기념일</p>
  </main>
</template>

<script lang="ts"></script>

<style scoped>
main {
  width: 100%;
  display: flex;
  align-items: center;
  gap: 1rem;
}
p:hover {
  color: green;
  text-decoration: underline;
  text-underline-offset: 0.5rem;
}
</style>
