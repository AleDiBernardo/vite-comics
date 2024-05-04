<script>
export default {
  props: {
    cardURL: String,
    cardPrice: String,
    cardSeries: String,
    cardType: String,
  },
};
</script>

<template>
  <div class="card" :class="cardType">
    <img :src="cardURL" :alt="cardSeries" />
    <h4>{{ cardSeries }}</h4>
  </div>
</template>

<style scoped lang="scss">
@use "./style/partials/variables" as *;
@use "./style/partials/mixins" as *;

.card {
  //   background-color: white;
  padding: 0.5rem;
  text-align: center;
  width: 200px;

  img {
    max-width: 100%;
    aspect-ratio: 1;
  }
}
</style>
