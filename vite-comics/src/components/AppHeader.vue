<script>
export default {
  data() {
    return {
      counter: 0,
      menuLinks: [
        {
          title: "characters",
          isActive: true,
        },
        {
          title: "comics",
          isActive: false,
        },
        {
          title: "movies",
          isActive: false,
        },
        {
          title: "TV",
          isActive: false,
        },
        {
          title: "games",
          isActive: false,
        },
        {
          title: "collectibles",
          isActive: false,
        },
        {
          title: "videos",
          isActive: false,
        },
        {
          title: "fans",
          isActive: false,
        },
        {
          title: "news",
          isActive: false,
        },
        {
          title: "shop",
          isActive: false,
        },
      ],
    };
  },
  methods: {
    checkActive: function (index) {
      this.menuLinks[this.counter].isActive = false;
      this.counter = index;
      this.menuLinks[this.counter].isActive = true;
    },
  },
};
</script>

<template>
  <header>
    <div class="container">
      <a href="#">
        <img src="../assets/img/dc-logo.png" alt="" id="logo" />
      </a>
      <ul>
        <li
          v-for="(link, index) in menuLinks"
          :class="{ active: link.isActive }"
          @click="checkActive(index)"
        >
          <a href="#">
            {{ link.title.toUpperCase() }}
          </a>
        </li>
      </ul>
    </div>
  </header>
</template>

<style scoped lang="scss">
@use "./style/partials/variables" as *;
@use "./style/partials/mixins" as *;

header {
  background-color: $header-color;
  height: 100px;

  .container {
    // Mixin Flex
    padding: 0;
    @include flex(row, space-between, center);
    height: 100%;

    #logo {
      max-width: 80%;
    }

    ul {
      @include flex(row, space-between, center);
      gap: 2rem;
      list-style: none;
      font-family: monospace;
      font-weight: bold;
      font-size: 1rem;
      height: 100%;

      li {
        @include flex(row, space-between, center);

        height: 100%;

        &.active {
          border-bottom: 3px solid blue;
          border-color: $primary-color;
          a {
            color: $primary-color;
          }
        }
        a {
          color: $header-text-color;
        }
      }
    }
  }
}
</style>
