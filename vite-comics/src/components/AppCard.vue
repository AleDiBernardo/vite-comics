<script>
export default {
  props: {

    cardObj: Object
  },
};
</script>

<template>
  
  <div
    class="card"
    :class="cardObj.type === 'comic book' ? 'comicBook' : 'graphicNovel'"
  >
    <img :src="cardObj.thumb" :alt="cardObj.series" />
    <a href="#"><h4>{{ cardObj.series }}</h4></a>
  </div>
</template>

<style scoped lang="scss">
@use "./style/partials/mixins" as *;

.card {
  @include flex(row, center, center, wrap);
  padding: 0.5rem;
  text-align: center;
  gap: 10px;
  cursor: pointer;

  &.comicBook {
    border: 2px solid red;
  }

  &.graphicNovel {
    border: 2px solid yellow;
  }

  &:hover {
    // border-width: 4px;
    background-color: lightyellow;
    color: black;
  }

  img {
    max-width: 100%;
    aspect-ratio: 1;
    position: relative;
  }
  a{
    text-decoration: none;
    color: inherit;
    h4 {
      text-transform: uppercase;
      font-size: 0.7rem;
      
    }
  }
}
</style>
