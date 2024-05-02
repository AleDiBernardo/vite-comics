<script>
export default {
  data() {
    return {
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
};
</script>

<template>
  <header>
    <div class="container">
      <img src="../assets/img/dc-logo.png" alt="" />
      <ul>
        <li v-for="link in menuLinks">
          <a href="#" :class="{active: link.isActive}">
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
}

.container {
  // Mixin Flex
  @include flex(row, space-between, center);


  ul {
    @include flex(row, space-between, center);
    gap: 2rem;
    list-style: none;
    font-family: monospace;
    font-weight: bold;
    font-size: 1rem;

    li{
        a{
            text-decoration: none;
            color: $header-text-color;

            &:hover{
                color: $primary-color;
            }

            &.active{
                border-bottom: 4px;
                border-color: $primary-color; 
            }
        }


    }

  }
}
</style>
