<template>
  <div :class="{'banner__active': isHover }" class="banner">
    <div class="banner__container">
      <div class="banner__block">
        <div class="banner__title">Dubai IT Company</div>
        <n-button v-on:mouseenter="isHover = true" v-on:mouseleave="isHover = false" class="banner__btn">Learn More
        </n-button>
      </div>
    </div>
    <img class="banner__img" src="../assets/images/banner.jpeg" alt="banner">
    <div>lorem *42</div>
  </div>
</template>

<script setup>
import {ref} from 'vue'

const isHover = ref(false)
</script>

<style lang="scss" scoped>
@import '../assets/styles/mixins.scss';

.banner {
  position: relative;
  width: 100%;
  min-height: calc(100vh + 60px);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

  &::before {
    transition: $trn;
    content: '';
    z-index: 2;
    width: 100%;
    height: 100%;
    position: absolute;
    background: rgba(0, 0, 0, 0.5);
    left: 0;
    top: 0;
  }

  &::after {
    content: '';
    z-index: 3;
    width: 100%;
    position: absolute;
    background: linear-gradient(0deg, rgba(1, 23, 59, 0.99) 1%, rgba(161, 176, 203, 0) 100%);
    left: 0;
    bottom: 0;
    @include fluid(height, 30px, 60px);
  }

  &__active {
    &::before {
      background: rgba(0, 0, 0, 0);
    }
  }


  &__container {
    @include container;
    z-index: 3;
  }

  &__block {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: center;

  }

  &__img {
    z-index: 1;
    width: 100%;
    height: 100%;
    position: absolute;
    opacity: 1;
    left: 0;
    top: 0;
    object-fit: cover;
  }

  &__title {
    color: #fff;
    @include fluid(font-size, 38px, 60px);
    @include fluid(margin-bottom, 10px, 20px);
    font-weight: 600;
  }

  &__btn {
    @include fluid(padding-top, 10px, 25px);
    @include fluid(padding-bottom, 10px, 25px);
    @include fluid(padding-right, 20px, 50px);
    @include fluid(padding-left, 20px, 50px);
    @include fluid(font-size, 16px, 18px);
    border-radius: 25px;
    width: fit-content;
    font-weight: 600;
    background: rgba(33, 177, 255, 0.7);
    color: #fff;

    &:hover {
      background: rgba(33, 177, 255, 0.9);
      color: #fff;
    }
  }
}
</style>