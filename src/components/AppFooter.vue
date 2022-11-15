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
            <h3>Shop</h3>
            <ul>
              <li><a href="#">Shop DC</a></li>
              <li><a href="#">Shop DC Collectibles</a></li>
            </ul>
          </div>
          <div class="ctr">
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
            <h3>Shop</h3>
            <ul>
              <li><a href="#">Shop DC</a></li>
              <li><a href="#">Shop DC Collectibles</a></li>
            </ul>
          </div>
          <div class="rgt">
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
            <h3>Shop</h3>
            <ul>
              <li><a href="#">Shop DC</a></li>
              <li><a href="#">Shop DC Collectibles</a></li>
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
        @include startFlex;
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
        }
      }
      .right {
        img {
          transform: translateY(-1%);
          width: 95%;
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
          width: 120px;
          background-color: $secondary-color;
          text-transform: uppercase;
          color: $primary-color;
          border: 1px solid $tertiary-color;
          padding: 8px 10px;
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
