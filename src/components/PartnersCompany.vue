<template>
  <div class="partners">
    <my-title title="We cooperate with these companies" />
    <n-scrollbar x-scrollable>
      <div class="partners__block">
        <img
          class="partners__img"
          src="../assets/images/mic.svg"
          alt="partners"
        />
        <img
          class="partners__img"
          src="../assets/images/company2.png"
          alt="partners"
        />
        <img
          class="partners__img"
          src="../assets/images/company4.png"
          alt="partners"
        />
        <img
          class="partners__img"
          src="../assets/images/company5.png"
          alt="partners"
        />
        <img
          class="partners__img"
          src="../assets/images/company6.png"
          alt="partners"
        />
      </div>
    </n-scrollbar>
  </div>
</template>

<script setup>
import MyTitle from "./MyTitle.vue";
</script>

<style lang="scss" scoped>
@import "../assets/styles/mixins.scss";

.partners {
  @include container;
  @include fluid(margin-bottom, 25px, 50px);

  &__container {
    overflow-x: scroll;
  }

  &__block {
    display: flex;
    align-items: center;
    width: max-content;
    @include fluid(padding-bottom, 15px, 30px);
  }

  &__img {
    @include fluid(height, 40px, 53px);
    width: 20%;
    margin-right: 30px;
    object-fit: contain;
    transition: $trn;
    filter: invert(70%) sepia(6%) saturate(0%) hue-rotate(164deg)
      brightness(88%) contrast(83%);

    &:hover {
      filter: none;
    }
  }
}
</style>
