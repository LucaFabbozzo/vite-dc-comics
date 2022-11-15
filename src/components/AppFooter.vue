<script>
export default {
  name: "AppFooter",
};
</script>

<template>
  <footer>
    <div class="top">
      <div class="container tp">
        <div class="left">
          <div class="lft">
            <h3>Dc comics</h3>
            <ul>
              <li><a href="#">Characters</a></li>
              <li><a href="#">Comics</a></li>
              <li><a href="#">Movies</a></li>
              <li><a href="#">TV</a></li>
              <li><a href="#">Games</a></li>
              <li><a href="#">Videos</a></li>
              <li><a href="#">News</a></li>
            </ul>
            <h3 class="shop">Shop</h3>
            <ul>
              <li><a href="#">Shop DC</a></li>
              <li><a href="#">Shop DC Collectibles</a></li>
            </ul>
          </div>
          <div class="ctr">
            <h3>Dc</h3>
            <ul>
              <li><a href="#">Therm of use</a></li>
              <li><a href="#">Privacy policy new</a></li>
              <li><a href="#">Add Choices</a></li>
              <li><a href="#">Advertising</a></li>
              <li><a href="#">Jobs</a></li>
              <li><a href="#">Subscription</a></li>
              <li><a href="#">Talent Workshops</a></li>
              <li><a href="#">CPSC Certificates</a></li>
              <li><a href="#">Ratings</a></li>
              <li><a href="#">Shop help</a></li>
              <li><a href="#">Contact us</a></li>
            </ul>
          </div>
          <div class="rgt">
            <h3>Sites</h3>
            <ul>
              <li><a href="#">DC</a></li>
              <li><a href="#">MAD Magazine</a></li>
              <li><a href="#">DC kids</a></li>
              <li><a href="#">DC Universe</a></li>
              <li><a href="#">DC Power Visa</a></li>
            </ul>
          </div>
        </div>

        <div class="right">
          <img src="/dc-logo-bg.png" alt="logo-footer" />
        </div>
      </div>
    </div>

    <div class="bottom">
      <div class="container icons">
        <div class="right">
          <button>Sign-up Now!</button>
        </div>
        <div class="left">
          <p>Follow Us</p>
          <img src="../assets/img/footer-facebook.png" alt="facebook" />
          <img src="../assets/img/footer-twitter.png" alt="twitter" />
          <img src="../assets/img/footer-youtube.png" alt="youtube" />
          <img src="../assets/img/footer-pinterest.png" alt="pinterest" />
          <img src="../assets/img/footer-periscope.png" alt="periscope" />
        </div>
      </div>
    </div>
    <div class="down">
      <div class="container"></div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;
footer {
  .top {
    height: 275px;
    background-image: url("../assets/img/footer-bg.jpg");
    overflow: hidden;
    .tp {
      height: 100%;
      @include betweenFlex;
      .left {
        margin-top: 50px;
        height: 100%;
        @include startFlex;
        .lft,
        .ctr {
          margin-right: 20px;
          .shop {
            margin-top: 20px;
          }
        }

        h3 {
          text-transform: uppercase;
          font-size: 0.9rem;
        }
        ul {
          li {
            list-style: none;
          }
          a {
            text-decoration: none;
            font-size: 0.6rem;
          }
          a:hover {
            color: $primary-color;
          }
        }
      }
      .right {
        img {
          transform: translateX(25%);
          width: 80%;
        }
      }
    }
  }
  .bottom {
    height: 80px;
    background-color: $secondary-color;
    .icons {
      height: 100%;
      @include betweenFlex;
      .right {
        button {
          width: 125px;
          background-color: $secondary-color;
          text-transform: uppercase;
          color: $primary-color;
          border: 2px solid $tertiary-color;
          padding: 10px;
          cursor: pointer;
        }
      }
      .left {
        @include centerFlex;
        p {
          margin-right: 15px;
          text-transform: uppercase;
          color: $tertiary-color;
        }
        img {
          margin-right: 15px;
          width: 25px;
        }
      }
    }
  }
  .down {
    height: 30px;
    background-color: #212121;
  }
}
</style>
