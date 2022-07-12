<template>
  <div class="about">
    <my-title title="About us" />
    <div class="conviction">
      <div v-motion-slide-visible-left class="conviction__block">
        <div class="conviction__item">
          <div class="conviction__title">Our team</div>
          <div class="conviction__text">
            We not only believe, but know that many things in software
            development industry can be dealt better – from design to
            development and support. We united to create a company that is
            complete – taking care of every step of your project, through
            designs, development and testings, to finally releasing your product
            in the best shape.
          </div>
        </div>
        <img class="conviction__img" src="../assets/images/about-2.png" />
      </div>
      <div v-motion-slide-visible-right class="conviction__block">
        <div class="conviction__mini">
          <div class="conviction__title">Perfect code</div>
          <div class="conviction__text">
            Big enough to be flexible, small enough to care. Many people think
            that Literate Programming is just a documenting system or a
            formatting system for ordinary comments. In fact, a program with
            little to no comments can be written using the Literate Programming
            approach, just as verbose notes by themselves do not create a
            Literate Programming approach.
          </div>
        </div>
        <img class="conviction__img" src="../assets/images/about-1.png" />
      </div>
    </div>
  </div>
</template>

<script setup>
import MyTitle from "./MyTitle.vue";
</script>

<style lang="scss" scoped>
@import "../assets/styles/mixins.scss";

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
      flex-direction: column-reverse;
    }
  }

  &__mini {
    @include fluid(margin-top, 15px, 30px);
  }

  &__img {
    @include fluid(height, 290px, 443px);
    width: 100%;
    object-fit: contain;
  }

  &__title {
    @include fluid(margin-bottom, 15px, 30px);
    @include fluid(line-height, 20px, 37px);
    @include fluid(font-size, 24px, 32px);
    font-weight: 600;
    color: $primary;
  }

  &__text {
    @include fluid(line-height, 16px, 24px);
    @include fluid(font-size, 14px, 16px);
    @include fluid(margin-bottom, 15px, 30px);
    font-weight: 500;
    width: 84%;
  }
}

@media screen and (max-width: 992px) {
  .conviction {
    flex-direction: column;

    &__block {
      width: 100%;
      margin-bottom: 30px;

      &:nth-child(2n) {
        width: 100%;
        flex-direction: column;
      }
    }

    &__text {
      width: 100%;
    }
  }
}

@media screen and (max-width: 576px) {
  .conviction {
    &__img {
      height: 220px;
    }
  }
}
</style>
