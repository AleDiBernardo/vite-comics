<script>
export default {
  data() {
    return {
      icons: [
        {
          image: "buy-comics-digital-comics.png",
          text: "digital comics",
        },
        {
          image: "buy-comics-merchandise.png",
          text: "dc merchandise",
        },
        {
          image: "buy-comics-subscriptions.png",
          text: "subscription",
        },
        {
          image: "buy-comics-shop-locator.png",
          text: "comics shop locator",
        },
        {
          image: "buy-dc-power-visa.svg",
          text: "dc power visa",
        },
      ],
    };
  },
  methods: {
    getImagePath(curImage) {
      return new URL(`../assets/img/${curImage}`, import.meta.url).href;
    },
  },
};
</script>

<template>
  <div id="icons-ctn">
    <div class="container">
      <ul>
        <li v-for="icon in icons">
          <a href="#">
            <div>
                <img :src="getImagePath(icon.image)" alt="" />
            </div>
          <span>{{ icon.text.toUpperCase()}}</span>
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<style scoped lang="scss">
@use "./style/partials/variables" as *;
@use "./style/partials/mixins" as *;

#icons-ctn {
  background-color: $primary-color;
  position: relative;
  z-index: 1;
  min-height: 220px;

  .container {
    padding: 4rem;
    ul {
      @include flex(row, space-between, center);
      li {
        a{

          @include flex(row, space-between, center);
          
          
        }
        list-style: none;
        span{
            font-size: 15px;
        }
        img {
          width: 60%;
        }

        &:last-child{
            width: 15%;
        }

        &:hover{
          border-bottom: 2px solid white;
        }

      }
    }
  }
}
</style>
