<template>
  <div class="support">
    <div :class="{'support__block-active': isHover }" class="support__block">
      <div class="support__item">
        <div class="support__title">{{ title }}</div>
        <div class="support__text">{{ text }}
        </div>
        <n-button
            v-on:mouseenter="isHover = true"
            v-on:mouseleave="isHover = false"
            class="support__btn">
          Apply
        </n-button>
      </div>
      <img :src="img" alt="banner" class="support__img">
    </div>
  </div>
</template>

<script setup>
import {ref} from 'vue'

const props = defineProps({
  title: {
    type: String,
    required: true
  },
  text: {
    type: String,
    required: true
  },
  to: {
    type: String,
    required: true
  },
  img: {
    type: String,
    required: true
  },
  background: String
});


const isHover = ref(false)
</script>

<style lang="scss" scoped>
@import '../assets/styles/mixins.scss';

.support {
  @include container;
  @include fluid(margin-bottom, 25px, 50px);

  &__block {
    display: flex;
    align-items: flex-end;
    justify-content: space-between;
    backdrop-filter: blur(12px);
    position: relative;
    border: 1px solid rgba(255, 255, 255, 0.5);
    border-radius: 10px;
    overflow: hidden;

    &::before {
      transition: $trn;
      content: '';
      z-index: 2;
      width: 100%;
      height: 100%;
      position: absolute;
      background: rgba(0, 0, 0, 0.2);
      left: 0;
      top: 0;
    }

    &-active {
      &::before {
        background: rgba(0, 0, 0, 0);
      }
    }
  }


  &__item {
    width: 48%;
    position: relative;
    z-index: 3;
    @include fluid(padding, 50px, 100px);
  }

  &__img {
    @include fluid(height, 300px, 544px);
    transition: $trn;
    position: relative;
    width: 50%;
    z-index: 1;
    object-fit: cover;

  }

  &__title {
    @include fluid(font-size, 28px, 48px);
    @include fluid(margin-bottom, 15px, 25px);
    font-weight: 700;
    color: #fff;
  }

  &__text {
    @include fluid(margin-bottom, 25px, 50px);
    @include fluid(font-size, 22px, 36px);
    font-weight: 500;
    color: #fff;
  }

  &__btn {
    @include fluid(padding-top, 10px, 25px);
    @include fluid(padding-bottom, 10px, 25px);
    @include fluid(padding-right, 50px, 100px);
    @include fluid(padding-left, 50px, 100px);
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

@media screen and (max-width: 992px) {
  .support {
    &__block {
      padding-top: 100px;
      padding-bottom: 100px;
      padding-left: 30px;
      padding-right: 30px;

      &::before {
        background: rgba(0, 0, 0, 0.6);
      }
    }

    &__item {
      width: 100%;
      padding: 0;
    }

    &__img {
      width: 100%;
      height: 100%;
      object-fit: contain;
      position: absolute;
      bottom: 0;
    }
  }
}

@media screen and (max-width: 768px) {
  .support {
    &__block {
      padding-top: 50px;
      padding-bottom: 50px;

      &::before {
        background: rgba(0, 0, 0, 0.2)
      }
    }

    &__img {
      display: none;
    }
  }
}
</style>