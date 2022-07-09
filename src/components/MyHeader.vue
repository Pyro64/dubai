<template>
  <header>
    <div class="block">
      <my-logo :logo="logo"/>
      <div class="item">
        <my-nav/>
        <n-button c>Contact us</n-button>
      </div>
    </div>
  </header>
</template>

<script setup>
import MyLogo from "./MyLogo.vue";
import MyNav from "./MyNav.vue";
import logo from "../assets/images/logo.png";</script>

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

</style>
