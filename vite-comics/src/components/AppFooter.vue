<script>
export default {
  data() {
    return {
      dc_comics_links: [
        "Characters",
        "Comics",
        "Movies",
        "TV",
        "Games",
        "Videos",
        "News",
      ],
      dc_shop_links: ["Shop DC", "Shop DC Collectibles"],
      dc_links: [
        "Terms Of Use",
        "Privacy policy (New)",
        "Ad Choices",
        "Advertising",
        "Jobs",
        "Subscriptions",
        "Talent Workshops",
        "CPSC Certificates",
        "Ratings",
        "Shop Help",
        "Contact us"
      ],
      dc_sites: [
        "DC",
        "MAD Magazine",
        "DC Kids",
        "DC Universe",
        "DC Power Visa"
      ]
    };
  },
};
</script>

<template>
  <footer>
    <div class="footerTop">
      <div class="container">
        <div class="col">
          <div class="dc-comics">
            <span>dc comics</span>
            <ul v-for="link in dc_comics_links">
              <li>
                <a href="#">
                  {{ link }}
                </a>
              </li>
            </ul>
          </div>
          <div class="dc-shop">
            <span>shop</span>
            <ul v-for="link in dc_shop_links">
                <li>
                <a href="#">
                  {{ link }}
                </a>
              </li>
            </ul>
          </div>
        </div>
        <div class="col">
          <span>DC</span>
          <ul v-for="link in dc_links">
                <li>
                <a href="#">
                  {{ link }}
                </a>
              </li>
            </ul>
        </div>
        <div class="col">
          <span>sites</span>
          <ul v-for="link in dc_sites">
                <li>
                <a href="#">
                  {{ link }}
                </a>
              </li>
            </ul>
        </div>
      </div>
    </div>
    <div class="footerBottom">
      <div class="container">s</div>
    </div>
  </footer>
</template>

<style scoped lang="scss">
@use "./style/partials/variables" as *;
@use "./style/partials/mixins" as *;

footer {
  .footerTop {
    //   background-color: lightgreen;
    background-image: url("../assets/img/footer-bg.jpg");
    // height: 400px;

    .container {
      @include flex(row, flex-start, flex-start);
      gap: 10px;
      font-size: 25px;

      .col {
        padding: 0.5rem;
        // background-color: lightcoral;

        span {
          text-transform: uppercase;
        }

        li {
          list-style: none;
          font-size: 20px;
          padding: 5px;

          a{
            text-decoration: none;
            color: $footer-text-color;

            &:hover{
                color: $primary-color;
            }
          }
        }

        .dc-comics {
          margin-bottom: 20px;
        }
      }
    }
  }
  .footerBottom {
    background-color: lightblue;
    height: 80px;
  }
}
</style>
