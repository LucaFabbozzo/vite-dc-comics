<script>
export default {
  name: "AppMain",
};
</script>

<template>
  <div class="main">
    <div class="top">
      <div class="container">
        <h1>Content goes here</h1>
      </div>
    </div>
    <div class="button"></div>
  </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;
.top {
  @include centerFlex;
  background-color: #1c1c1c;
  height: 100px;
  font-size: 0.6rem;
}
</style>
