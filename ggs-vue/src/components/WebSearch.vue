<template>
  <div id="panel">
    <div id="left_sec">
      <Logo :need_icon="need_icon" />
      <div id="search">
        <span id="search_icon"></span>
        <div id="stick"></div>
        <input id="search_text" class="idpw" placeholder="Search" type="text" />
      </div>
    </div>

    <div id="pmenu">
      <Category />
    </div>
  </div>
</template>

<script lang="ts">
import Logo from './Logo.vue'
import Category from './Category.vue'

export default {
  components: {
    Logo,
    Category,
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
  border-bottom: 0.1rem solid rgba(255, 255, 255, 0.5);
  margin-bottom: 1rem;
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  flex-direction: column;
}

#left_sec {
  height: 4rem;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: row;
  gap: 1rem;
}
#stick {
  width: 0.1rem;
  height: 50%;
  background-color: white;
  opacity: 0.5;
}

#login {
  height: 70%;
  width: auto;
  aspect-ratio: 1 / 1;
  background-image: url('/unknown_user.svg');
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}
#search {
  height: 60%;
  width: 20%;

  line-height: 100px;
  display: flex;
  align-items: center;
  justify-items: center;

  flex-direction: row-reverse;
  padding: 0 1rem 0 1rem; /* 상오하왼 */
  border-radius: 1rem;
  background-color: rgba(0, 0, 0, 0.5);
  /* border: 0.1rem solid white; */
  gap: 0.5rem;
}
#search_text {
  height: 100%;
  width: 90%;
}
#search_icon {
  height: 50%;
  width: auto;

  aspect-ratio: 1 / 1;
  background-image: url('/search.svg');
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}
</style>
