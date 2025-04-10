<template>
<main>

  <div id="product">
    <div id="event">{{ event }}</div>
    <div id="img"></div>
    <div id="name">{{ name }}</div>
    <div id="price">{{ price }}원</div>
  </div>

</main>
</template>

<script lang="ts">
export default {
  props: {
    event: {
      type: String,
      required: false,
    },
    name: {
      type: String,
      required: true,
    },
    price: {
      type: String,
      required: true,
    },
  },
}
</script>

<style scoped>
main {
  width: 100%;
  display: flex;
  justify-content: center;
  gap: 3rem;
  padding: 1rem;
}

#event{
  position: absolute;
  /* margin: 0.5rem; */
  background-color: rgba(200, 0, 0, 0.8);
  padding: 0.5rem;
  border-radius: 0.5rem 0 0.5rem 0;
  border: 0.2rem solid white;
}
#img{
  border-radius: 0.5rem;
  width: 100%; height: 20rem;
  background-color: gray;
}
#price{
  font-size: 1.5rem;
  font-weight: 600;
}
</style>
