<template>
  <transition>
    <div :class="{ active: isbool }" class="preloader">
      <img class="logo" src="../assets/images/logo.svg" :logo="logo" />
    </div>
  </transition>
</template>
<script setup>
import MyLogo from "./MyLogo.vue";
import logo from "../assets/images/logo.svg";
import { useTimeoutPoll } from "@vueuse/core";
import { ref } from "vue";
const isbool = ref(false);
setTimeout(() => {
  isbool.value = true;
}, 5000);
</script>
<style scoped lang="scss">
@import "../assets/styles/mixins.scss";
.preloader {
  height: 100vh;
  width: 100vw;
  content: "";
  display: flex;
  align-items: center;
  justify-content: center;
  position: fixed;
  top: 0;
  left: 0;
  backdrop-filter: blur(10px);
  background: rgba(0, 0, 0, 0.7);
  z-index: 10;
  transition: 0.38s ease-in-out;
  opacity: 1;
  transform: scale(1);
}
.active {
  opacity: 0;
  transform: scale(0);
}

.logo {
  @include fluid(width, 100px, 200px);
  @include fluid(height, 100px, 200px);
  object-fit: contain;
}
</style>
