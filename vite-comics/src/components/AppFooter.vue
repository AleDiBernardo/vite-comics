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
        "Contact us",
      ],
      dc_sites: [
        "DC",
        "MAD Magazine",
        "DC Kids",
        "DC Universe",
        "DC Power Visa",
      ],
      link_icons: ["fa-brands fa-twitter", "fa-brands fa-facebook", "fa-brands fa-youtube", "fa-brands fa-pinterest", "fa-solid fa-location"],
    };
  },
};
</script>

<template>
  <footer>
    <div class="footerTop">
      <div class="container">
        <div class="col-container">
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

        <div class="logo"></div>
        <!-- <img src="../assets/img/dc-logo-bg.png" alt="" /> -->
      </div>
    </div>

    <div class="footerBottom">
      <div class="container">
        <a href="#">Sign Up Now!</a>
        <div class="socials">
          <a href="#">follow us</a>

          <ul>
            <!-- TODO: add icons -->
            <li v-for="icon in link_icons">
              <a href="#">
                <i :class="icon"></i>
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<style scoped lang="scss">
@use "./style/partials/variables" as *;
@use "./style/partials/mixins" as *;

footer {
  .footerTop {
    background-image: url("../assets/img/footer-bg.jpg");

    .container {
      @include flex(row, space-between, flex-start);
      gap: 10px;
      font-size: 18px;
      position: relative;

      .logo {
        width: 500px;
        aspect-ratio: 1;
        position: absolute;
        top: -50px;
        right: 80px;
        background-repeat: no-repeat;
        background-size: contain;
        background-image: url("../assets/img/dc-logo-bg.png");
      }

      .col-container {
        @include flex(row, space-between, flex-start);

        .col {
          padding: 0.5rem;
          // background-color: lightcoral;

          span {
            text-transform: uppercase;
          }

          li {
            list-style: none;
            font-size: 15px;
            padding: 5px;

            a {
              text-decoration: none;
              color: $footer-text-color;

              &:hover {
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
  }
  .footerBottom {
    background-color: $footer-color;
    font-weight: bold;

    // height: 80px;
    position: relative;
    height: 100%;
    z-index: 1;
    font-size: 20px;
    .container {
      @include flex(row, space-between, center);

      a {
        padding: 15px 20px;
        border: 3px solid $primary-color;
        text-decoration: none;
        color: inherit;
        text-transform: uppercase;
      }

      li {
        list-style: none;
      }
      .socials {
        @include flex(row, center, center);

        a {
          padding: 15px 20px;
          border: none;
          text-decoration: none;
          color: $primary-color;
          text-transform: uppercase;
          &:hover{
            color: inherit
          }
        }

        ul {
          @include flex(row, center, center);
          gap: 10px;

          li{
            a{
              color: inherit;
              &:hover {
                color: $primary-color;
              }
            }
          }
        }
      }
    }
  }
}
</style>
