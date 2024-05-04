<script>
import { cardsArray } from "../assets/data/cards";
import AppCard from "./AppCard.vue";
export default {
  components: {
    AppCard,
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
      <h1>Current Series</h1>

      <div class="row">
        <div class="col" v-for="card in cards">
          <AppCard
            :cardURL="card.thumb"
            :cardSeries="card.series"
            :cardType="card.type"
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
  padding: 80px 0;
  position: relative;

  .container {
    h1 {
      position: absolute;
      top: -30px;
      font-size: 30px;
      margin-bottom: 30px;
      padding: 20px;
      position: absolute;
      // top: 0px;
      background-color: $primary-color;
      text-transform: uppercase;
    }

    .row {
      @include flex(row, space-between, stretch, wrap);

      gap: 20px;
      .col {
        width: calc(100% / 6 - 20px);
        // margin-bottom: 1rem;
      }
    }
  }
}
</style>
