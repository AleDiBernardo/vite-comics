<script>
import { cardsArray } from '../assets/data/cards';
import AppCard from './AppCard.vue'
export default {
  components: {
    AppCard
  },
  data() {
    return {
      cards: cardsArray,
    };
  },
};
</script>

<template>
  <main>
    <div class="container">
      <h1>I Nostri Prodotti</h1>

      <div class="row">
        <div class="col" v-for="card in cards">
          <AppCard 
            :cardURL="card.thumb"
            :cardSeries="card.series"
          />
        </div>
      </div>
    </div>
  </main>
</template>

<style scoped lang="scss">
@use "./style/partials/variables" as *;
@use "./style/partials/mixins" as *;

main {
  background-color: $main-color;
  padding: 60px 0;

  .container {

    h1 {
      font-size: 35px;
      margin-bottom: 30px
    }
  
    .row {
      @include flex(row, space-between, stretch, wrap);
  
      .col {
        width: calc(100% / 6);
        margin-bottom: 1rem;
      }
    }
  }
}
</style>
