<script>
export default {
  name: "AppFooter",
};
</script>

<template>
  <footer>
    <div class="top">
      <div class="container"></div>
    </div>
    <div class="bottom">
      <div class="container"></div>
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
    background-image: url("..assets/img/footer-bg.jpg");
  }
  .bottom {
    height: 80px;
    background-color: $secondary-color;
  }
  .down {
    height: 30px;
    background-color: #212121;
  }
}
</style>
