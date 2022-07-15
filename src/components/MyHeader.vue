<template>
  <header>
    <div class="block">
      <my-logo :logo="logo" />
      <div class="item">
        <div class="header__wrapper">
          <my-nav />
        </div>
        <n-button c>Contact us</n-button>
      </div>
    </div>
  </header>
</template>

<script setup>
import MyLogo from "./MyLogo.vue";
import MyNav from "./MyNav.vue";
import logo from "../assets/images/logo.svg";
</script>

<style lang="scss" scoped>
@import "../assets/styles/mixins.scss";

header {
  @include fluid(padding-top, 10px, 10px);
  @include fluid(padding-bottom, 10px, 10px);
  position: fixed;
  z-index: 10;
  top: 0;
  width: 100%;
  background: rgba(51, 51, 51, 0.6);
  backdrop-filter: blur(10px);
  box-shadow: 0px 10px 20px rgba(33, 177, 255, 0.2);
}

.block {
  @include container;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.item {
  display: flex;
  align-items: center;
  justify-content: center;
}

@media screen and (max-width: 768px) {
  .block {
    position: relative;
    padding-bottom: 30px;
  }
  .header {
    &__wrapper {
      overflow-x: scroll;
      position: absolute;
      bottom: 0;
      width: 100%;
      left: 15px;
    }
  }
}
</style>
