<template>
  <div class="about">
    <my-title title="About us"/>
    <div class="conviction">
      <div class="conviction__block">
        <div class="conviction__title">Our team</div>
        <div class="conviction__text">
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
          enim ad minim veniam, quis nostrud exercitation ullamco laboris
          nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in
          reprehenderit in voluptate velit esse cillum dolore eu fugiat
          nulla pariatur. Excepteur sint occaecat cupidatat non proident,
          sunt in culpa qui officia deserunt mollit anim id est laborum."
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
          enim ad minim veniam, quis nostrud exercitation ullamco laboris
          nisi ut aliquip ex ea commodo consequat.
        </div>
        <img class="conviction__img" src="../assets/images/about-2.png"/>
      </div>
      <div class="conviction__block">
        <div class="conviction__text">
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
          enim ad minim veniam, quis nostrud exercitation ullamco laboris
          nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in
          reprehenderit in voluptate velit esse cillum dolore eu fugiat
          nulla pariatur. Excepteur sint occaecat cupidatat non proident,
          sunt in culpa qui officia deserunt mollit anim id est laborum."
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
          enim ad minim veniam, quis nostrud exercitation ullamco laboris
          nisi ut aliquip ex ea commodo consequat.
        </div>
        <div class="conviction__title">Perfect code</div>
        <img class="conviction__img" src="../assets/images/about-1.png"/>
      </div>
    </div>
  </div>

</template>

<script setup>
import MyTitle from "./MyTitle.vue";</script>

<style lang="scss" scoped>
@import '../assets/styles/mixins.scss';

.about {
  @include container;
  @include fluid(margin-top, 25px, 50px);
  @include fluid(margin-bottom, 25px, 50px);
}

.conviction {
  display: flex;
  justify-content: space-between;
  @include fluid(padding-bottom, 30px, 100px);

  &__block {
    display: flex;
    flex-direction: column;
    width: 48%;
    @include fluid(margin-right, 75px, 135px);

    &:nth-child(2n) {
      margin-right: 0;
      width: 40%;
      flex-direction: column-reverse;

      .conviction__img {
        @include fluid(margin-bottom, 30px, 80px);
        margin-top: 0;
      }

      .conviction__text {
        width: 100%;
      }
    }
  }

  &__img {
    @include fluid(margin-top, 20px, 80px);
    @include fluid(height, 250px, 443px);
    width: 100%;
    object-fit: contain;

  }

  &__title {
    @include fluid(margin-bottom, 15px, 30px);
    @include fluid(line-height, 20px, 37px);
    @include fluid(font-size, 16px, 32px);
    font-weight: 600;
    color: $primary;
  }

  &__text {
    @include fluid(line-height, 16px, 24px);
    @include fluid(font-size, 14px, 16px);
    font-weight: 500;
    width: 84%;
  }
}
</style>