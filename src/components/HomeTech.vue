<template>
  <div class="tech">
    <my-title title="Technologies we work with"/>
    <div class="tech__block">
      <router-link to="/" class="tech__item" v-for="t in tech" :key="t.id">
        <img class="tech__svg" :src="t.src" :alt="t.text">
        <div class="tech__title">{{ t.text }}</div>
        <div class="tech__text">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consectetur culpa eum ex,
          incidunt iure iusto
          laudantium molestias, natus, nemo obcaecati quam quia? Aperiam consequuntur eum iure porro temporibus tenetur
          totam.
        </div>
      </router-link>
    </div>
  </div>

</template>

<script setup>
import MyTitle from "./MyTitle.vue";
import react from '../assets/images/icon/react.svg';
import angular from '../assets/images/icon/angular.svg';
import vue from '../assets/images/icon/vue.svg'
import c from '../assets/images/icon/c.svg'
import flutter from '../assets/images/icon/flutter.svg'
import python from '../assets/images/icon/python.svg'
import swift from '../assets/images/icon/swift.svg'
import java from '../assets/images/icon/java.svg'

const tech = [
  {
    id: 1,
    text: 'react',
    src: react,
  },
  {
    id: 2,
    text: 'angular',
    src: angular,
  },
  {
    id: 3,
    text: 'vue',
    src: vue,
  },
  {
    id: 4,
    text: 'c++',
    src: c,
  },
  {
    id: 5,
    text: 'flutter',
    src: flutter,
  },
  {
    id: 6,
    text: 'java',
    src: java,
  },
  {
    id: 7,
    text: 'swift',
    src: swift,
  },
  {
    id: 8,
    text: 'python',
    src: python,
  },
]
</script>

<style lang="scss" scoped>
@import '../assets/styles/mixins.scss';

.tech {
  @include fluid(margin-bottom, 25px, 50px);
  @include container;

  &__block {
    display: flex;
    flex-wrap: wrap;
  }

  &__item {
    @include fluid(padding-top, 20px, 40px);
    @include fluid(padding-bottom, 20px, 40px);
    @include fluid(padding-right, 20px, 40px);
    @include fluid(padding-left, 20px, 40px);
    transition: $trn;
    border-radius: 15px;
    width: 20%;
    margin-right: 6.6%;
    margin-bottom: 5%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    border: 1px solid $light;

    &:nth-child(4n) {
      margin-right: 0;
    }

    &:hover {
      @include hover;

      .about {
        &__svg {
          opacity: 1;
        }
      }
    }
  }

  &__svg {
    @include fluid(width, 30px, 60px);
    @include fluid(height, 30px, 60px);
    @include fluid(margin-bottom, 10px, 20px);
    transition: $trn;
    opacity: 0.8;
    object-fit: contain;
  }

  &__title {
    @include fluid(font-size, 14px, 18px);
    @include fluid(margin-bottom, 10px, 20px);
    text-transform: uppercase;
    font-weight: 600;
  }

  &__text {
    text-align: center;
  }
}

</style>